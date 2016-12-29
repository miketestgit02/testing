###purpose of this page
you clone down https://github.com/murjax/Github-Repo-Submodulizer<br>... remove the .git file and then paste it into github submodulizer. <br>both my_repositories and Testing

###map of testing environment
<pre>
`cmd tree`
.
├── 1_test_CheckReadmeAndSubdirs
│   ├── 1_result_repo
│   │   ├── 1_1_result
│   │   │   └── README.md
│   │   └── 2_1_result
│   ├── 2_result_repo
│   │   ├── 1_2_result
│   │   └── 2_2_result
│   │       ├── 2_2_1_result
│   │       │   └── README.md
│   │       ├── 2_2_2_result
│   │       └── README.md
│   ├── README.md
│   └── e_NoSubReadme
└── 2_test_MasterRepoNoSub
    └── README.md
</pre>


It could be that this command is the trouble.

cd Testing/;rm -rf *; rm -rf .*; cd ../; cd my_repositories/; rm -rf *; rm -rf .*;

cd ../../testing/; cp -r * ../Github-Repo-Submodulizer/Testing/; cp -r * ../Github-Repo-Submodulizer/my_repositories/;

cd ../Github-Repo-Submodulizer; rake submodulize_folder;
