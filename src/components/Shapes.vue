<script>
  export default {
    name: 'Shapes',

    render() {
      function getRandomLength() {
        return Math.floor(Math.random() * 500 + 100);
      }

      function getRandomGap() {
        return Math.floor(Math.random() * 500 + 900);
      }

      return (
        <div class="shape-container" style={{ overflow: 'hidden' }}>
          <svg
            class="svg-shapes"
            xmlns="http://www.w3.org/2000/svg"
            version="1.1"
            viewBox="100 100 600 600"
            preserveAspectRatio="xMidYMid slice"
          >
            {[0, 1, 2, 3, 4].map((item) => (
              <circle
                key={item}
                r={Math.floor(Math.random() * 900) + 100}
                cx={Math.floor(Math.random() * 900)}
                cy={Math.floor(Math.random() * 900)}
                stroke-width={Math.floor(Math.random() * 200 + 75)}
                stroke-dasharray={`${getRandomLength()} ${getRandomGap()}`}
              />
            ))}
          </svg>
          <svg style={{ pointerEvents: 'none' }}>
            <defs>
              <linearGradient id="bggrad" x1="0%" y1="0%" x2="100%" y2="100%">
                <stop offset="0%" style={{ stopColor: '#E9336B' }} />
                <stop
                  offset="100%"
                  style={{ stopColor: '#ff8674' }}
                />
              </linearGradient>
            </defs>
          </svg>
        </div>
      )
    }
  }
</script>

<style>
  .shape-container {
    position: absolute;
    top: 0;
    left: 0;
    bottom: 0;
    right: 0;
    width: 100vw;
    height: 100vh;
  }

  .svg-shapes {
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    width: 100vw;
    height: 100%;
    margin: 0;
  }

  .svg-shapes circle {
    fill: transparent;
    stroke: url(#bggrad);
    stroke-linecap: round;
    animation: bgmove 200s linear infinite;
  }

  @keyframes bgmove {
    0% {
      stroke-dashoffset: 1000;
    }

    100% {
      stroke-dashoffset: 0;
    }
  }
</style>
