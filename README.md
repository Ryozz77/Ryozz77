name: Bug Report
description: File a bug report to FiveM, RedM, FXServer, or FxDK, excluding crashes
labels: ["bug", "triage"]
assignees:
  - 

body:
  - type: markdown
    attributes:
      value: |
        Thank you for taking the time to fill out this bug report.
        Only bug related issues are accepted, so please refrain from submitting any other requests (including support requests).
        
        \* Issue reports that fail to deliver the proper information may be closed without any feedback.
  
  - type: textarea
    id: what-happened
    attributes:
      label: What happened?
      description: |
        Please be clear and concise
      placeholder: 
    validations:
      required: true

  - type: input
    id: expectation
    attributes:
      label: Expected result
      description: |
        What should've happened instead?
    validations:
      required: true

  - type: textarea
    id: repro
    attributes:
      label: Reproduction steps
      description: |
        This is important to us. Fill in the exact steps you took, test and remove any steps that aren't relevant.
      placeholder: |
        1. 
        2. 
        3. 
        4. 
    validations:
      required: true

  - type: dropdown
    id: importancy
    attributes:
      label: Importancy
      description: |
        To your knowledge how would you describe the importancy of this bug?
      options:
        - Unknown
        - Slight inconvenience
        - There's a workaround
        - Security issue
        - Crash
    validations:
      required: true

  - type: dropdown
    id: areas
    attributes:
      label: Area(s)
      multiple: true
      description: |
        Which of the following areas does this issue apply to? Please mark all that apply.
      options:
        - FiveM
        - RedM
        - FXServer
        - FxDK
        - 'OneSync'
        - 'Natives'
        - 'ScRT: Lua'
        - 'ScRT: C#'
        - 'ScRT: JS'
    validations:
      required: true

  - type: input
    id: build-number
    attributes:
      label: Specific version(s)
      description: Please fill in the build numbers of the product(s) this issue occured on
      placeholder: FiveM/RedM 6464, Server 6402 windows/linux
    validations:
      required: true

  - type: textarea
    id: misc
    attributes:
      label: Additional information
      description: |
        Anything else you'd like to add?
 13 changes: 13 additions & 0 deletions13  
.github/ISSUE_TEMPLATE/config.yml
@@ -0,0 +1,13 @@
blank_issues_enabled: false
contact_links:
  - name: Public Documentation (docs.fivem.net)
    url: https://github.com/citizenfx/fivem-docs
    about: For all docs.fivem.net related requests and issues

  - name: FiveM native documentation
    url: https://github.com/citizenfx/natives
    about: For issues related to FiveM game natives

  - name: RedM native documentation
    url: https://github.com/citizenfx/natives_rdr3
    about: For issues related to RedM game natives
 77 changes: 77 additions & 0 deletions77  
.github/ISSUE_TEMPLATE/docs_improvement.yml
@@ -0,0 +1,77 @@
name: Documentation Improvement
description: Improve request for FiveM, RedM, or FXServer's documentation
labels: ["documentation", "triage"]
assignees:
  - 

body:
  - type: markdown
    attributes:
      value: |
        Thank you for taking the time to fill out this documentation improvement request.
        Only documentation related requests are accepted, so please refrain from submitting any other requests (including support requests).
        
        Any requests on documentation found on https://docs.fivem.net/docs/ need to go to https://github.com/citizenfx/fivem-docs.
        
        \* Requests that fail to deliver the proper information may be closed without any feedback.
  
  - type: input
    id: segment 
    attributes:
      label: Segment
      description: |
        Which segment is this targeting? e.g.: type, method, field, or property
      placeholder: 
    validations:
      required: true

  - type: dropdown
    id: importancy
    attributes:
      label: Importancy
      description: |
        To your knowledge how would you describe the importancy of this feature?
      options:
        - Unknown
        - Nice extra
        - Missing details
        - Unclear or unintuitive
        - Incorrect
    validations:
      required: true

  - type: textarea
    id: improvement
    attributes:
      label: Improvement request
      description: |
        Tell us what needs to be changed to make this better, also add suggestions if you have any
    validations:
      required: true

  - type: dropdown
    id: areas
    attributes:
      label: Area(s)
      multiple: true
      description: |
        Which of the following areas does this request apply to? Please mark all that apply.
      options:
        - FiveM
        - RedM
        - FXServer
        - FxDK
        - 'OneSync'
        - 'Natives'
        - 'ScRT: Lua'
        - 'ScRT: C#'
        - 'ScRT: JS'
    validations:
      required: true

  - type: textarea
    id: misc
    attributes:
      label: Additional information
      description: |
        Anything else you'd like to add?
 74 changes: 74 additions & 0 deletions74  
.github/ISSUE_TEMPLATE/feature_request.yml.disabled
@@ -0,0 +1,74 @@
name: Feature Request
description: Need FiveM, RedM, or FXServer to support something?
labels: ["enhancement", "triage"]
assignees:
  - 

body:
  - type: markdown
    attributes:
      value: |
        Thank you for taking the time to fill out this feature request.
        Only feature requests are accepted, so please refrain from submitting any other requests (including support requests).

        \* Requests that fail to deliver the proper information may be closed without any feedback.

  - type: textarea
    id: goal
    attributes:
      label: Goal
      description: |
        Please be clear and concise and make sure you focus on the **X** in [XY Problems](https://xyproblem.info/)
      placeholder: 
    validations:
      required: true

  - type: dropdown
    id: importancy
    attributes:
      label: Importancy
      description: |
        To your knowledge how would you describe the importancy of this feature?
      options:
        - Unknown
        - Nice extra
        - Quality of Life (QoL)
        - Overall quality to the platform
        - Prerequisite for my project
        - Fatal (we can't use the platform without)

  - type: textarea
    id: implementation
    attributes:
      label: API and/or potential implementation
      description: |
        Tell us what the user interface will look like and maybe a potential implementation
    validations:
      required: true

  - type: dropdown
    id: areas
    attributes:
      label: Area(s)
      multiple: true
      description: |
        Which of the following areas does this request apply to? Please mark all that apply.
      options:
        - FiveM
        - RedM
        - FXServer
        - FxDK
        - 'OneSync'
        - 'Natives'
        - 'ScRT: Lua'
        - 'ScRT: C#'
        - 'ScRT: JS'
    validations:
      required: true

  - type: textarea
    id: misc
    attributes:
      label: Additional information
      description: |
        Anything else you'd like to add?
 38 changes: 38 additions & 0 deletions38  
.github/PULL_REQUEST_TEMPLATE.md
@@ -0,0 +1,38 @@
### Goal of this PR
<!-- Consice explanation of what this PR meant to achieve -->
@blattersturm
blattersturm 3 days ago Contributor
Concise? My browser highlighted this as a spelling error while making a PR.


...


### How is this PR achieving the goal

...


### This PR applies to the following area(s)
<!-- Add any that applies, e.g.: FiveM, RedM, Server, Natives, FxDK, ScRT: Lua, ScRT: C#, ScRT: JS, etc. -->

...


### Successfully tested on
<!-- Add any that is applicable, remove any that aren't. -->

**Game builds:** .. 

**Platforms:** Windows, Linux


### Checklist
<!-- Mark all points with x that apply, i.e.: [x]. -->

- [ ] Code compiles and has been tested successfully.
- [ ] Code explains itself well and/or is documented.
- [ ] My commit message explains what the changes do and what they are for.
- [ ] No extra compilation warnings are added by these changes.


### Fixes issues
<!-- Add any issue that this PR fixes with: `fixes #123`, `resolves #234`, `closes #345`. -->


 136 changes: 136 additions & 0 deletions136  
.github/workflows/ci/build_linux.sh
@@ -0,0 +1,136 @@
#JOB_SLOTS=16
ROOT_REPO=$(pwd)
ROOT_DEP=${1:-/tmp}
JOB_SLOTS=${2:-16}

# install compile-time dependencies
sudo apt-get -y install libstdc++6 gcc-multilib lua5.3 lua5.3-dev \
	libcurl4-openssl-dev libssl-dev libv8-dev libc-ares-dev libclang-dev libv8-dev \
	python3-venv make clang lld dotnet-sdk-6.0 \
	build-essential unzip 

# symlinks
#sudo ln -s /lib/x86_64-linux-gnu/libclang-15.so.15 /lib/x86_64-linux-gnu/libclang.so
sudo ln -s /usr/lib/x86_64-linux-gnu/libclang-10.so /usr/lib/x86_64-linux-gnu/libclang.so
sudo ln -s /usr/lib/x86_64-linux-gnu/libcurl.so /usr/lib/libcurl.so

# install python deps
python3 -m venv $ROOT_DEP/py-venv
. $ROOT_DEP/py-venv/bin/activate

pip install ply six Jinja2 MarkupSafe

# build natives
cd $ROOT_REPO/ext/natives
gcc -O2 -shared -fpic -o cfx.so -I/usr/include/lua5.3/ lua_cfx.c

mkdir -p inp out
curl --http1.1 -sLo inp/natives_global.lua http://runtime.fivem.net/doc/natives.lua

cd $ROOT_REPO/ext/native-doc-gen

ROOT_NATIVE_GEN=$(pwd)
LUA53=lua5.3
NODE=node            
YARN="$NODE $ROOT_NATIVE_GEN/yarn_cli.js"

# install yarn deps
cd $ROOT_NATIVE_GEN/../native-doc-tooling/

echo yarn
$YARN global add node-gyp@9.3.1
$YARN

cd $ROOT_NATIVE_GEN/../natives/

NATIVES_MD_DIR=$ROOT_NATIVE_GEN/../native-decls/native_md/ $LUA53 codegen.lua inp/natives_global.lua markdown server rpc

# make out dir
mkdir -p "$ROOT_NATIVE_GEN/out" && cd "$_"

# build
$NODE $ROOT_NATIVE_GEN/../native-doc-tooling/index.js $ROOT_NATIVE_GEN/../native-decls/

mkdir -p $ROOT_NATIVE_GEN/../natives/inp/ || true

echo build2
NODE_PATH=$ROOT_NATIVE_GEN/../native-doc-tooling/node_modules/ $NODE $ROOT_NATIVE_GEN/../native-doc-tooling/build-template.js lua CFX > $ROOT_NATIVE_GEN/../natives/inp/natives_cfx_new.lua

# copy outputs
cd $ROOT_NATIVE_GEN
cp -a out/natives_test.json natives_cfx.json

# copy new
if [ -e $ROOT_NATIVE_GEN/../natives/inp/natives_cfx.lua ]; then
	if ! diff -q $ROOT_NATIVE_GEN/../natives/inp/natives_cfx_new.lua $ROOT_NATIVE_GEN/../natives/inp/natives_cfx.lua 2>&1 > /dev/null; then
		cp -a $ROOT_NATIVE_GEN/../natives/inp/natives_cfx_new.lua $ROOT_NATIVE_GEN/../natives/inp/natives_cfx.lua
	fi
else
	cp -a $ROOT_NATIVE_GEN/../natives/inp/natives_cfx_new.lua $ROOT_NATIVE_GEN/../natives/inp/natives_cfx.lua
fi


cd $ROOT_REPO/ext/natives

mkdir -p ~/natives/cfx-server/citizen/scripting/lua/
mkdir -p ~/natives/cfx-server/citizen/scripting/v8/

lua5.3 codegen.lua inp/natives_global.lua native_lua server > $ROOT_REPO/code/components/citizen-scripting-lua/include/NativesServer.h
lua5.3 codegen.lua inp/natives_global.lua lua server > ~/natives/cfx-server/citizen/scripting/lua/natives_server.lua
lua5.3 codegen.lua inp/natives_global.lua js server > ~/natives/cfx-server/citizen/scripting/v8/natives_server.js
lua5.3 codegen.lua inp/natives_global.lua dts server > ~/natives/cfx-server/citizen/scripting/v8/natives_server.d.ts

cat > $ROOT_REPO/code/client/clrcore/NativesServer.cs << EOF
#if IS_FXSERVER
using ContextType = CitizenFX.Core.fxScriptContext;
namespace CitizenFX.Core.Native
{
EOF

lua5.3 codegen.lua inp/natives_global.lua enum server >> $ROOT_REPO/code/client/clrcore/NativesServer.cs
lua5.3 codegen.lua inp/natives_global.lua cs server >> $ROOT_REPO/code/client/clrcore/NativesServer.cs

cat >> $ROOT_REPO/code/client/clrcore/NativesServer.cs << EOF
}
#endif
EOF

lua5.3 codegen.lua inp/natives_global.lua cs_v2 server > $ROOT_REPO/code/client/clrcore-v2/Native/NativesServer.cs

lua5.3 codegen.lua inp/natives_global.lua rpc server > ~/natives/cfx-server/citizen/scripting/rpc_natives.json

# done with natives

# download and build premake
curl --http1.1 -sLo $ROOT_DEP/premake.zip https://github.com/premake/premake-core/releases/download/v5.0.0-beta1/premake-5.0.0-beta1-src.zip

cd $ROOT_DEP
unzip -q premake.zip
rm premake.zip
cd premake-*

cd build/gmake*.unix/
make -j${JOB_SLOTS}
cd ../../

mv bin/release/premake5 /usr/local/bin
cd ..

rm -rf premake-*

## SETUP-CUTOFF

# build CitizenFX
cd $ROOT_REPO/code

premake5 gmake2 --game=server --cc=clang --dotnet=msnet
cd build/server/linux

export CFLAGS="-fno-plt"
export CXXFLAGS="-D_LIBCPP_ENABLE_CXX17_REMOVED_AUTO_PTR -Wno-deprecated-declarations -Wno-invalid-offsetof -fno-plt"
export LDFLAGS="-Wl,--build-id -fuse-ld=lld -ldl"

make clean
make clean config=release verbose=1
make -j${JOB_SLOTS} config=release
 20 changes: 20 additions & 0 deletions20  
.github/workflows/ci/build_windows.sh
@@ -0,0 +1,20 @@
pwsh ./fxd.ps1 get-chrome
./prebuild.cmd

pwsh ./fxd.ps1 gen -game $PROGRAM

cd code/build/$PROGRAM/$([[ $PROGRAM = server ]] && echo windows || echo '')

"C:\Program Files\Microsoft Visual Studio\2022\Enterprise\MSBuild\Current\Bin\MsBuild.exe" CitizenMP.sln -t:build -restore -p:RestorePackagesConfig=true -p:preferredtoolarchitecture=x64 -p:configuration=release -maxcpucount:4 -v:q -fl1 "-flp1:logfile=errors.log;errorsonly"
MSBUILD_ERROR=$?

if [[ $MSBUILD_ERROR -eq 0 ]]; then
	echo Successfully build $PROGRAM
else
	RED=$'\e[31m'

	echo "::error::Failed to build $PROGRAM, MSBuild returned with error code: $MSBUILD_ERROR"
	while IFS= read -r LINE; do echo "$RED$LINE"; done < errors.log

	exit $MSBUILD_ERROR
fi
 68 changes: 68 additions & 0 deletions68  
.github/workflows/ci_build.yml
@@ -0,0 +1,68 @@
name: CI Build all products

on:
  workflow_call:

jobs:
  build_all:
    strategy:
      matrix:
        builds:
          - [ FiveM,  five,   windows ]
          - [ RedM,   rdr3,   windows ]
          - [ Server, server, windows ]
          #- [ Server, server, linux   ]
    name: ${{ matrix.builds[0] }}${{ matrix.builds[2] == 'linux' && ' (Linux)' || '' }}
    runs-on: ${{ matrix.builds[2] == 'windows' && 'windows-latest' || 'ubuntu-20.04' }}
    env:
      PROGRAM: ${{ matrix.builds[1] }}
      PLATFORM: ${{ matrix.builds[2] }}      
    steps:
      - name: Checkout
        shell: bash
        run: |          
          # Settings
          #  - Windows: D is too small, C is big enough, checkout action doesn't allow this.
          [[ $PLATFORM = windows ]] && ROOT="C:\b" || ROOT=~/b
          ROOT_REPO="$ROOT/$PROGRAM"
          ROOT_DEP="$ROOT/dep"
          JOB_SLOTS=$(nproc --all);
          #JOB_SLOTS=$((JOB_SLOTS * 2)) # can cause heap allocation issues on Windows
          
          # Share with other steps
          echo "ROOT_REPO=$ROOT_REPO" >> "$GITHUB_ENV"
          echo "ROOT_DEP=$ROOT_DEP" >> "$GITHUB_ENV"
          echo "JOB_SLOTS=$JOB_SLOTS" >> "$GITHUB_ENV"
          
          # Checkout all repos
          mkdir -p "$ROOT_REPO" && cd "$_" || exit 1
          
          # Call each git command individually, preventing unnecessary checkouts
          git init .
          git config core.symlinks true
          git remote add origin https://github.com/$GITHUB_REPOSITORY.git
          git pull origin $GITHUB_REF:PR_BRANCH --depth=1
          git submodule update --jobs=$JOB_SLOTS --init --depth=1
        
      - name: Dependencies
        shell: bash
        run: |
          mkdir -p "$ROOT_DEP" && cd "$_" || exit 1
          
          echo Downloading boost
          curl -s -L https://boostorg.jfrog.io/artifactory/main/release/1.71.0/source/boost_1_71_0.7z -o boost.7z
          7z -bso0 x boost.7z -oboost
          rm boost.7z
          echo "BOOST_ROOT=$PWD\boost\boost_1_71_0" >> "$GITHUB_ENV"
        
      - name: Compile
        shell: bash
        run: |
          cd "$ROOT_REPO"
          
          # messes with current build tools, so clear it
          BUILD_SCRIPT=".github/workflows/ci/build_$PLATFORM.sh"
          PLATFORM= # clear out, some other scripts consider this variable
          
          chmod +x "$BUILD_SCRIPT"
          $BUILD_SCRIPT "$ROOT_DEP" $JOB_SLOTS
 33 changes: 33 additions & 0 deletions33  
.github/workflows/issue_closed.yml
@@ -0,0 +1,33 @@
name: Remove triage
on:
  issues:
    types: [ closed, deleted ]
  pull_request:
    types: [ closed, deleted ]

jobs:
  label_issues:
    runs-on: ubuntu-latest
    permissions:
      issues: write
    steps:
      - uses: actions/github-script@v6
        with:
          script: |
            try
            {
                await github.rest.issues.removeLabel({
                    issue_number: context.issue.number,
                    owner: context.repo.owner,
                    repo: context.repo.repo,
                    name: ["triage"]
                });
            }
            catch (exception)
            {
                // we don't care if the label wasn't present, as long as it's gone now
                if (exception.status !== 404)
                {
                    console.log(exception);
                }
            }
 81 changes: 81 additions & 0 deletions81  
.github/workflows/issue_opened.yml
@@ -0,0 +1,81 @@
name: Label issues
on:
  issues:
    types:
      - reopened
      - opened
env:
  ISSUE_BODY: ${{ github.event.issue.body }}
  ISSUE_TITLE: ${{ github.event.issue.title }}

jobs:
  label_issues:
    runs-on: ubuntu-latest
    permissions:
      issues: write
    steps:
      - uses: actions/github-script@v6
        with:
          script: |
            const issue = {
                issue_number: context.issue.number,
                owner: context.repo.owner,
                repo: context.repo.repo
            };
            
            // Is the title long enough to convey any useful meaning?
            if (process.env.ISSUE_TITLE.length < 10)
            {
              github.rest.issues.createComment({
                ...issue,
                body: "Closing this issue, the title is too short to convey any real meaning, please create another issue with an explanatory title."
              });
              
              github.rest.issues.update({
                ...issue,
                state: "closed",
                state_reason: "not_planned"
              });
              
              return;
            }
            
            // labels
            {
              var addLabels = ["triage"];
              
              const issueBody = process.env.ISSUE_BODY;
              
              const areasStringRegex = /### Area\(s\)\s*(.*)/;
              const areasLabels = [ "FxDK", "RedM", "ScRT: Lua", "ScRT: C#", "ScRT: JS" ];
              
              var areasString = areasStringRegex.exec(issueBody);
              if (areasString && areasString.length > 1)
              {
                var areas = areasString[1].split(/\s*[,\n]\s*/);
                for (var i = 0; i < areas.length; ++i)
                {
                  const area = areas[i];
                  if (areasLabels.includes(area))
                  {
                    addLabels.push(area);
                  }
                }
              }
              
              const priorityStringRegex = /### Importancy\s*(.*)/;
              
              var priorityString = priorityStringRegex.exec(issueBody);
              if (priorityString)
              {
                switch (priorityString[1])
                {
                  case "Crash": addLabels.push("crash"); break;
                }
              }
            
              github.rest.issues.addLabels({
                ...issue,
                labels: addLabels
              });
            }
 214 changes: 214 additions & 0 deletions214  
.github/workflows/pr_opened.yml
@@ -0,0 +1,214 @@
name: Validate PR
on:
  pull_request:
    types: [ reopened, opened, edited, synchronize, ready_for_review ]
    paths:
      - 'code/**'
      - '!.github/**'
      - '!code/tools/**'
      - '!ext/**'
      - '!*.bat'
      - '!*.cmd'
      - '!*.ps1'
      - '!*.psm1'
      - '!*.sh'

permissions:
  pull-requests: write

concurrency:
  group: ${{ github.workflow }}-${{ github.event.pull_request.number || github.ref }}
  cancel-in-progress: true

jobs:
  input_validation:
    name: Validate PR details
    if: github.event.pull_request.draft == false
    runs-on: ubuntu-latest
    env:
      COMMITS_URL: ${{ github.event.pull_request.commits_url }}
      PR_TITLE: ${{ github.event.pull_request.title }}
      PR_DESCR: ${{ github.event.pull_request.body }}
      PR_HEAD_SHA: ${{ github.event.pull_request.head.sha }}
      PR_BASE_SHA: ${{ github.event.pull_request.base.sha }}
      PR_GITHUB_CONTEXT: ${{ toJSON(github) }}
    steps:
      - name: Check PR details
        run: |
          valid=true
          
          if [[ ${#PR_TITLE} -lt 10 ]]; then
            echo "::error::PR title is too small to convey any real meaning."
            valid=false
          fi
          
          if [[ ${#PR_DESCR} -lt 10 ]]; then
            echo "::error::PR body is too small to convey any real meaning."
            valid=false
          fi
          
          if [[ $valid = false ]]; then
            exit 1
          fi
      
      - name: Check commit titles
        run: |
          # get commits json and make an array of commit messages
          readarray -t commitMessages < <(curl -ks "$COMMITS_URL" | jq '.[].commit.message' )
          
          # requires at least 8 characters in description
          commitTitleRegex="^(tweak|fix|feat)\([a-zA-Z0-9\/-]+\): .{8,}"
          valid=true
          
          for (( i=0; i < ${#commitMessages[@]}; i++ )); do
            # remove first and last " (quotes) and get title from message (ends at the first '\n' or the end of the string)
            title=${commitMessages[$i]:1:-1}
            title=${title%%\\n*}
            
            if [[ "$title" =~ $commitTitleRegex ]]; then
              echo "         valid title: $title"
            else
              echo "::error::Invalid title: $title"
              valid=false
            fi
          done
          
          if [[ $valid = false ]]; then
            echo '::error::One or more of your commit titles do not conform to our title rules'
            echo 
            echo 'Titles need to:'
            echo '- Start with: fix, tweak, or feat,'
            echo '- Within parenthesis contain the area the change is applying,'
            echo '- Colon + space, i.e: ": \",'
            echo '- Description longer than 8 characters".'
            echo 
            echo 'Examples of correct commit titles:'
            echo '- fix(clrcore): something I fixed'
            echo '- feat(scripting/lua): new feature for lua'
            echo '- tweak(scripting/v8): some tweaks'
            exit 1
          fi
      
      - name: Label it
        uses: actions/github-script@v6
        with:
          script: |
            const issue = {
                issue_number: context.issue.number,
                owner: context.repo.owner,
                repo: context.repo.repo
            };
            
            var addLabels = [ ];
              
            const issueBody = process.env.PR_DESCR;
            
            const areasStringRegex = /### This PR applies to the following area\(s\)\s*(?:<!--.*?-->\s*)*(.*?)(?=\n#)/s;
            const areasLabels = [ "FxDK", "RedM", "ScRT: Lua", "ScRT: C#", "ScRT: JS" ];
              
            var areasString = areasStringRegex.exec(issueBody);            
            if (areasString && areasString.length > 1)
            {
              var areas = areasString[1].split(/\s*[,\n]\s*/);
              for (var i = 0; i < areas.length; ++i)
              {
                const area = areas[i];
                if (areasLabels.includes(area))
                {
                  addLabels.push(area);
                }
              }
            }
            
            if (addLabels.length > 0)
            {
              // triage label
              github.rest.issues.addLabels({
                ...issue,
                labels: addLabels
              });
            }
  
  build_all:
    name: Build
    needs: input_validation
    uses: ./.github/workflows/ci_build.yml

  post_build:
    name: Post Build PR actions
    if: always()
    needs: build_all
    runs-on: ubuntu-latest
    steps:
      - name: Mark PR as valid
        if: ${{ !contains(needs.*.result, 'failure') }}
        uses: actions/github-script@v6
        with:
          script: |
            const issue = {
                issue_number: context.issue.number,
                owner: context.repo.owner,
                repo: context.repo.repo
            };
            
            // triage label
            github.rest.issues.addLabels({
                ...issue,
                labels: ["triage"]
            });
            
            // remove invalid
            try
            {
                await github.rest.issues.removeLabel({
                    ...issue,
                    name: ["invalid"]
                });
            }
            catch (exception)
            {
                // we don't care if the label wasn't present, as long as it's gone now
                if (exception.status !== 404)
                {
                    console.log(exception);
                }
            }
      
      - name: Mark PR as invalid
        if: ${{ contains(needs.*.result, 'failure') }}
        uses: actions/github-script@v6
        with:
          script: |
            const issue = {
                issue_number: context.issue.number,
                owner: context.repo.owner,
                repo: context.repo.repo
            };
            
            /*github.rest.issues.createComment({
                ...issue,
                body: "One or more of your commit titles do not conform to our title rules, make sure they all follow the following pattern: `type(component): description`. Allowed types are: `fix`, `tweak`, or `feat` and description must at least be 10 characters long to convey any meaning."
            });*/
            
            // invalid label
            github.rest.issues.addLabels({
                ...issue,
                labels: ["invalid"]
            });
            
            // remove triage
            try
            {
                await github.rest.issues.removeLabel({
                    ...issue,
                    name: ["triage"]
                });
            }
            catch (exception)
            {
                // we don't care if the label wasn't present, as long as it's gone now
                if (exception.status !== 404)
                {
                    console.log(exception);
                }
            }
