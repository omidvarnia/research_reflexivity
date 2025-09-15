🔍 𝗦𝗲𝗹𝗳-𝗥𝗲𝘃𝗶𝗲𝘄𝗶𝗻𝗴 𝗠𝘆 𝗢𝘄𝗻 𝗥𝗲𝘀𝗲𝗮𝗿𝗰𝗵: 𝗣𝗮𝗽𝗲𝗿 #𝟱



👉 𝗥𝗲𝗮𝗱 𝘁𝗵𝗲 𝗜𝗻𝘁𝗿𝗼𝗱𝘂𝗰𝘁𝗶𝗼𝗻 𝗣𝗼𝘀𝘁 𝗵𝗲𝗿𝗲: https://lnkd.in/eS_FjQHF



✅ 𝗣𝗮𝗽𝗲𝗿: Dynamic regional phase synchrony (DRePS): An Instantaneous Measure of Local fMRI Connectivity Within Spatially Clustered Brain Areas

𝗝𝗼𝘂𝗿𝗻𝗮𝗹: Human Brain Mapping, 2016



✅ 𝗥𝗲𝘃𝗶𝗲𝘄𝗲𝗿 #𝟮 𝗖𝗼𝗺𝗺𝗲𝗻𝘁𝘀



1. 𝗡𝗼𝘃𝗲𝗹𝘁𝘆 𝗶𝘀 𝗼𝘃𝗲𝗿𝘀𝘁𝗮𝘁𝗲𝗱: The concept of phase synchrony in fMRI wasn’t new in 2016; this was more of an incremental tweak to existing phase-based connectivity metrics.



2. 𝗠𝗮𝘁𝗵𝗲𝗺𝗮𝘁𝗶𝗰𝗮𝗹 𝗿𝗶𝗴𝗼𝗿 𝗴𝗮𝗽𝘀: While Hilbert-transform theory is referenced, the validation of assumptions (e.g., Bedrosian conditions) was only superficially addressed.



3. 𝗦𝗶𝗺𝘂𝗹𝗮𝘁𝗶𝗼𝗻 𝗼𝘃𝗲𝗿𝘀𝗶𝗺𝗽𝗹𝗶𝗳𝗶𝗰𝗮𝘁𝗶𝗼𝗻: The synthetic data are too clean to reflect the complex noise and physiological confounds in real BOLD data.



4. 𝗟𝗶𝗺𝗶𝘁𝗲𝗱 𝗰𝗼𝗵𝗼𝗿𝘁: Only 20 healthy controls; results lack statistical power and external validity.



5. 𝗙𝗿𝗲𝗾𝘂𝗲𝗻𝗰𝘆 𝗯𝗮𝗻𝗱: The choice of using the frequency band of 0.03–0.07 Hz as the primary band is based more on empirical evidence than on theoretical justification.



6. 𝗣𝗵𝘆𝘀𝗶𝗼𝗹𝗼𝗴𝗶𝗰𝗮𝗹 𝗰𝗼𝗻𝗳𝗼𝘂𝗻𝗱𝘀: Respiration and cardiac noise weren’t fully modeled or removed, making some “synchrony” patterns questionable.



7. 𝗔𝗹𝗴𝗼𝗿𝗶𝘁𝗵𝗺 𝗲𝗳𝗳𝗶𝗰𝗶𝗲𝗻𝗰𝘆: The MATLAB implementation processed a dataset in ~40 seconds. For larger datasets like HCP or UK Biobank, this approach would be computationally prohibitive. There was no GPU acceleration, no parallel processing, and no memory optimization, all of which limited adoption and reproducibility.



8. 𝗕𝗶𝗼𝗹𝗼𝗴𝗶𝗰𝗮𝗹 𝗶𝗻𝘁𝗲𝗿𝗽𝗿𝗲𝘁𝗮𝘁𝗶𝗼𝗻 𝗿𝗶𝘀𝗸: Linking ultra-slow fluctuations to meaningful local networks is speculative without multimodal corroboration (e.g., EEG-fMRI).



9. 𝗖𝗹𝘂𝘀𝘁𝗲𝗿𝗶𝗻𝗴 𝘀𝘂𝗯𝗷𝗲𝗰𝘁𝗶𝘃𝗶𝘁𝘆: Gaussian mixture modeling with fixed component selection is arbitrary and risks overfitting.



10. 𝗢𝘃𝗲𝗿𝗴𝗲𝗻𝗲𝗿𝗮𝗹𝗶𝘇𝗲𝗱 𝗰𝗹𝗮𝗶𝗺𝘀: The suggestion that DRePS could become a biomarker for health and disease was premature given the early-stage validation.



✅ 𝗢𝘃𝗲𝗿𝗮𝗹𝗹 𝗔𝘀𝘀𝗲𝘀𝘀𝗺𝗲𝗻𝘁

The method, while technically intriguing, lacks sufficient biological and clinical evidence. Specificity to genuine neural events was not convincingly demonstrated.



✅ 𝗪𝗵𝗮𝘁 𝗜 𝘄𝗼𝘂𝗹𝗱 𝗱𝗼 𝗱𝗶𝗳𝗳𝗲𝗿𝗲𝗻𝘁𝗹𝘆 𝘁𝗼𝗱𝗮𝘆:

• Validate against ground-truth multimodal datasets (e.g., invasive electrophysiology)

• Use larger, open-access cohorts (e.g., HCP or UK Biobank)

• Improve computational efficiency with Python or GPU-accelerated implementations

• Integrate artifact removal pipelines to better isolate neural dynamics



✅ 𝗢𝘃𝗲𝗿𝗮𝗹𝗹 𝗾𝘂𝗮𝗹𝗶𝘁𝘆: Clever methodological tweak, but biologically fragile and oversold.



#Neuroimaging #fMRI #BrainConnectivity #ScientificIntegrity #Reviewer2OnMyPapers
