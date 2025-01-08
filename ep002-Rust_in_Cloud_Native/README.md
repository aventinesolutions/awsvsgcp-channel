# AWS vs GCP Channel
## Episode 2: Rust in Cloud Native or "Sneller Cold Starts Nodig? ... Leer Rust Lang"

### Cold Start Definition
* In serverless functions refer to the delay that occurs when a function is invoked for the first time
  after being idle for a while. This happens because the serverless platform needs to allocate resources
  and initialize the function's environment before it can execute the code.
* Why Cold Starts Matter
  1. **Latency**: Cold starts introduce additional latency, which can affect the performance
     of your application. Users might experience delays, especially if the function is invoked infrequently.
  2. **Experience**: For applications requiring quick responses, such as real-time data processing or interactive
     web applications, cold starts can degrade the user experience.
  3. **Scalability**: While serverless architectures are designed to scale automatically, cold starts can impact
     the time it takes to handle sudden spikes in traffic
* Mitigating Cold Starts
  1. **Concurrency**: Some cloud providers offer options to keep functions warm by pre-allocating resources,
     reducing the likelihood of cold starts
  2. **Function Code**: Reducing the size of your function and its dependencies can help minimize cold start
     times
  3. **Efficient Runtimes**: Choosing runtimes that initialize quickly, such as Node.js or Go, can also help
     reduce cold start latency
* Understanding and addressing cold starts is crucial for maintaining the performance and reliability of
  serverless applications.

### Rustlings
```shell
mkdir -vp ~/Desktop/workspace/rust-lang; cd ~/Desktop/workspace/rust-lang
rustc –verson
cargo –version
export PATH="${HOME}"/.cargo/bin:"${PATH}"
cargo install rustlings
rustlings init
cd rustlings
rustlings
# in another terminal
code .
```

### Links
* [Lambda Cold Starts Benchmark](https://maxday.github.io/lambda-perf) by [maxday](https://maxday.dev)
  - [maxday/lambda-perf](https://github.com/maxday/lambda-perf)
* [rust-lang/rustlings](https://github.com/rust-lang/rustlings)
* [Amazon Low Latency Runtime awslabs/llrt](https://github.com/awslabs/llrt)
* [Using the Amazon Linux 2023 Container for Lambdas](https://docs.aws.amazon.com/linux/al2023/ug/lambda.html)
* [GraalVM](https://www.graalvm.org/) an efficient Java VM for Cloud Native and Serverless Functions
