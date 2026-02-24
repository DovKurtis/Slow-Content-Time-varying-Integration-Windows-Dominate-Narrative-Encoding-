# Slow-Content-Time-varying-Integration-Windows-Dominate-Narrative-Encoding-

Long-Term Goal: Develop hyper-dynamic, hyper-individualized encoding models trained on continuous, real-world multimodal data (visual, auditory, physiological, neural) to help shift neural decoding from controlled experiments to more natural sensory experience and life history. 

Abstract: 

Understanding spoken language requires integrating information across timescales, from words to extended narrative structure. While distributed cortical networks encode semantic content during naturalistic listening, it remains unclear how temporal integration windows adapt dynamically to narrative context or vary across individuals.

We investigate how cortical semantic representations flexibly shift across timescales as a function of linguistic content. Using fMRI from the Narratives dataset, word-level transcripts were aligned to BOLD timeseries and embedded into a continuous semantic vector space via pretrained language models. Embeddings were convolved with the hemodynamic response function and smoothed across short (~2s), medium (~10s), and long (~30s) temporal kernels. For each timescale, ridge regression models were trained to predict voxelwise BOLD responses and evaluated on held-out data via predicted-versus-observed timecourse correlation. Kernel dominance was tracked continuously using sliding-window local model comparison, with softmax weighting to capture smooth transitions between integration regimes. Engagement was estimated from antagonism between attention and default mode networks and related to dynamic kernel weights.

We hypothesize that cortical semantic representations are supported by concurrent integration windows whose relative contributions vary by brain region, narrative content, and individual engagement state. This framework provides a principled approach for characterizing adaptive semantic processing and may inform future efforts in decoding internal speech from neural activity. 
Put simply, we hypothesize that brain function is profoundly complex: no simple one-to-one cause-effect mapping exists. 

Current stage: 

Implemented multi-timescale semantic encoding pipeline using naturalistic fMRI data from the Narratives (pieman) dataset. Aligned transcripts to BOLD timepoints, embedded with pretrained language models, and temporally integrated using 2/10/30s kernels. Trained Ridge on first half of story and evaluated on second. (left) 

Defined functional ROIs using cross-validated prediction alignment (top 2% of voxels). Within the master ROI, demonstrated that a single long-timescale (≈30s) model outperforms shorter and multi-scale models, indicating specialization for long-range semantic integration. Defined separate scale-optimized ROIs (top 2%). Even in these ROIs, the 30s timescale consistently achieved the highest accuracy. (middle) 

Developed a time-resolved dominance analysis using sliding-window correlation and softmax weighting to track dynamic shifts between 2/10/30s representations. Results show variation in dominant integration windows over the course of the story. (right) 

Next steps: 

Extend to film and multimodal stimuli using CLIP-style joint text–visual embeddings. Test integration windows beyond 30s to probe act-level semantic structure. Compare timescale tuning across subjects and stories to characterize individual variability and content-dependent adaptation. Evaluate whether dynamic kernel weights predict engagement, comprehension, and default-mode network modulation. Ultimately, integrate these models into scalable decoding frameworks for inner-speech and high-level narrative state. 






