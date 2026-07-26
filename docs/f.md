# Superscalar Processors

One of the limitations on our simple processors is that they can only do one thing at a time. The concept of parallel processing implies that more than one thing can be done during the same clock cycle. The terminology we use to describe parallel architectures is called Flynn’s Taxonomy.

## Single Instruction, Single Data (SSID)

SISD describes the kind of processors we have looked at. A single control unit fetches one instruction at a time and executes it against a single data stream.

## Single Instruction, Multiple Data (SMID)
SIMD describes processors which execute a single instruction against an array of data. This might be suitable for graphics operations.

## Multiple Instructions, Single Data (MISD)

MISD describes systems where the processors are in an array for fault tolerance. This is common on aircraft and in military equipment; the space shuttle for example had 5 computers based on IBM360 architecture.

## Multiple Instruction, Multiple Data (MIMD)

 MIMD describes distributed processing systems which are truly independent, where each processor is carrying out its own instructions on its own data. Modern multi-core superscalar processors operate in this way, high-end super computers also operate like this.




