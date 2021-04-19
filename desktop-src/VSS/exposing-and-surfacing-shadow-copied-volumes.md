---
description: En plus d’être accessibles par le biais de l’interface IVssBackupComponents au moyen de l’objet Device de sa copie, un demandeur peut rendre disponible un cliché instantané pour d’autres processus en tant qu’appareil en lecture seule monté.
ms.assetid: 0898c2dc-992a-411b-81df-4f5e129f6a80
title: Exposition et revêtement des volumes clichés instantanés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d684aa9b696facaf1caa3aa3102c6b1d7fc37409
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106532281"
---
# <a name="exposing-and-surfacing-shadow-copied-volumes"></a><span data-ttu-id="df106-103">Exposition et revêtement des volumes clichés instantanés</span><span class="sxs-lookup"><span data-stu-id="df106-103">Exposing and Surfacing Shadow Copied Volumes</span></span>

<span data-ttu-id="df106-104">En plus d’être accessibles par le biais de l’interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) au moyen de l' [*objet Device*](vssgloss-d.md)de sa copie, un demandeur peut rendre disponible un cliché instantané pour d’autres processus en tant qu’appareil en lecture seule monté.</span><span class="sxs-lookup"><span data-stu-id="df106-104">In addition to being accessed through the [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) interface by means of its copy's [*device object*](vssgloss-d.md), a requester can make a shadow copy available to other processes as a mounted read-only device.</span></span>

<span data-ttu-id="df106-105">Ce processus est connu sous le nom [*d’exposition d’un cliché instantané*](vssgloss-e.md)et est effectué à l’aide de la méthode [**IVssBackupComponents :: ExposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot) .</span><span class="sxs-lookup"><span data-stu-id="df106-105">This process is known as [*exposing a shadow copy*](vssgloss-e.md), and is performed using the [**IVssBackupComponents::ExposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot) method.</span></span>

<span data-ttu-id="df106-106">Un cliché instantané peut être exposé en tant que volume local (une lettre de lecteur ou associée à un dossier monté) ou un partage de fichiers.</span><span class="sxs-lookup"><span data-stu-id="df106-106">A shadow copy can be exposed as a local volume—assigned a drive letter or associated with a mounted folder—or as a file share.</span></span>

<span data-ttu-id="df106-107">Pour illustrer ce cas, envisagez d’utiliser un cliché instantané d’un volume sur le système exposedSys monté sur F : \\ sur dont la racine est les répertoires dirOne et dirTwo, et le fichier FileOne.</span><span class="sxs-lookup"><span data-stu-id="df106-107">To illustrate, consider a shadow copy made of a volume on the system exposedSys mounted at F:\\ on whose root are the directories dirOne and dirTwo, and the file FileOne.</span></span>

## <a name="exposing-a-shadow-copy-locally"></a><span data-ttu-id="df106-108">Exposition locale d’un cliché instantané</span><span class="sxs-lookup"><span data-stu-id="df106-108">Exposing a Shadow Copy Locally</span></span>

<span data-ttu-id="df106-109">Lorsqu’il est monté en tant que volume local, la racine du cliché instantané est toujours visible au niveau du point de montage (lettre de lecteur ou dossier monté) et tous les fichiers copiés par des clichés instantanés sont visibles.</span><span class="sxs-lookup"><span data-stu-id="df106-109">When mounted as a local volume, the shadow copy's root is always visible at the mount point (drive letter or mounted folder) and all the shadow-copied files are visible.</span></span>

<span data-ttu-id="df106-110">Si le cliché instantané a été exposé localement par le biais du dossier monté C : \\ ShadowOfF, vous trouverez tous les fichiers présents sur le disque monté à F : \\ au moment du cliché instantané disponible sous C : \\ ShadowOfF.</span><span class="sxs-lookup"><span data-stu-id="df106-110">If the shadow copy was locally exposed through the mounted folder C:\\ShadowOfF, you would find all files present on disk mounted at F:\\ at the time of the shadow copy available under C:\\ShadowOfF.</span></span> <span data-ttu-id="df106-111">L’examen de C : \\ ShadowOfF révèle deux répertoires, dirOne et dirTwo, et un fichier, fileOne, sous C : \\ ShadowOfF.</span><span class="sxs-lookup"><span data-stu-id="df106-111">Examining C:\\ShadowOfF would reveal two directories, dirOne and dirTwo, and one file, fileOne, under C:\\ShadowOfF.</span></span>

<span data-ttu-id="df106-112">Un appel à exposer localement le cliché instantané peut être :</span><span class="sxs-lookup"><span data-stu-id="df106-112">A call to locally expose the shadow copy might be:</span></span>

``` syntax
  IVssBackupComponents *pReq;
  VSS_ID snapID;
  PWSTR wszExposed;
  //    .
  //    .
  hr = pReg->ExposeSnapshot(
         snapID,                           // VSS_ID SnapshotId,
         NULL,                             // VSS_PWSZ wszPathFromRoot
         VSS_VOLSNAP_ATTR_EXPOSED_LOCALLY, // LONG lAttributes
         L"C:\ShadowOfF",                  // VSS_PWSZ wszExpose
         LPWSTR &wszExposed,               // VSS_PWSZ* pwszExposed
       );
```

<span data-ttu-id="df106-113">Si le cliché instantané a été correctement exposé localement, *wszExposed* doit contenir la chaîne de caractères larges « C : \\ ShadowOfF ».</span><span class="sxs-lookup"><span data-stu-id="df106-113">If the shadow copy was successfully exposed locally, *wszExposed* should contain the wide character string "C:\\ShadowOfF."</span></span>

<span data-ttu-id="df106-114">Le cliché instantané peut être non exposé ultérieurement en appelant [**IVssBackupComponentsEx2 :: UnexposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-unexposesnapshot).</span><span class="sxs-lookup"><span data-stu-id="df106-114">The shadow copy can later be unexposed by calling [**IVssBackupComponentsEx2::UnexposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-unexposesnapshot).</span></span>

<span data-ttu-id="df106-115">Seuls les clichés instantanés persistants, à savoir, les clichés instantanés créés à l’aide de VSS \_ CTX \_ NAS \_ Rollback ou VSS \_ \_ application \_ Rollback, peuvent être exposés localement.</span><span class="sxs-lookup"><span data-stu-id="df106-115">Only persistent shadow copies—that is, shadow copies created with either VSS\_CTX\_NAS\_ROLLBACK or VSS\_CTX\_APP\_ROLLBACK—can be exposed locally.</span></span>

## <a name="exposing-a-shadow-copy-as-a-remote-share"></a><span data-ttu-id="df106-116">Exposition d’un cliché instantané en tant que partage distant</span><span class="sxs-lookup"><span data-stu-id="df106-116">Exposing a Shadow Copy as a Remote Share</span></span>

<span data-ttu-id="df106-117">Vous pouvez également choisir de rendre le cliché instantané du disque monté sur F : \\ disponible en tant que partage de fichiers distant et d’exposer uniquement les données sous dirTwo en tant que partage de fichiers dirTwoOfF.</span><span class="sxs-lookup"><span data-stu-id="df106-117">Alternatively, you could choose to make the shadow copy of the disk mounted at F:\\ available as a remote file share, and expose only data under dirTwo as the file share dirTwoOfF.</span></span>

<span data-ttu-id="df106-118">Dans ce cas, les systèmes peuvent accéder au cliché instantané des fichiers sous F : \\ dirTwo en mappant \\ \\ exposedSys \\ dirTwoOfF en tant que lecteur réseau.</span><span class="sxs-lookup"><span data-stu-id="df106-118">In this case, systems could access the shadow copy of files under F:\\dirTwo by mapping \\\\exposedSys\\dirTwoOfF as a network drive.</span></span>

<span data-ttu-id="df106-119">Un appel permettant d’implémenter à distance d’exposer le cliché instantané en tant que partage peut être le suivant :</span><span class="sxs-lookup"><span data-stu-id="df106-119">A call to implement remote exposing the shadow copy as a share might be the following:</span></span>

``` syntax
  IVssBackupComponents *pReq;
  VSS_ID snapID;
  LPWSTR wszExposed;
  //    .
  //    .
  hr = pReg->ExposeSnapshot(
               snapID,                            // VSS_ID SnapshotId,
               L"\dirTwo",                        // VSS_PWSZ wszPathFromRoot
               VSS_VOLSNAP_ATTR_EXPOSED_REMOTELY, // LONG lAttributes
               L"dirTwoOfF",                      // VSS_PWSZ wszExpose
               LPWSTR &wszExposed,                // VSS_PWSZ* pwszExposed
       );
```

<span data-ttu-id="df106-120">Si le cliché instantané a été exposé à distance avec succès, *wszExposed* doit contenir la chaîne de caractères larges « dirTwoOfF ».</span><span class="sxs-lookup"><span data-stu-id="df106-120">If the shadow copy was successfully exposed remotely, *wszExposed* should contain the wide character string "dirTwoOfF."</span></span>

<span data-ttu-id="df106-121">Tout système qui mappe actuellement le partage réseau de dirTwoOfF peut se déconnecter de celui-ci, tout comme il peut se déconnecter de n’importe quel partage ordinaire.</span><span class="sxs-lookup"><span data-stu-id="df106-121">Any system currently mapping the network share of dirTwoOfF could disconnect from it, just as it might disconnect from any ordinary share.</span></span>

## <a name="surfacing-a-shadow-copy"></a><span data-ttu-id="df106-122">Revêtement d’un cliché instantané</span><span class="sxs-lookup"><span data-stu-id="df106-122">Surfacing a Shadow Copy</span></span>

<span data-ttu-id="df106-123">Un cliché [*instantané superficiel*](vssgloss-s.md) est un cliché instantané dans lequel le cliché instantané est connu pour l’espace de noms du gestionnaire de montage d’un système.</span><span class="sxs-lookup"><span data-stu-id="df106-123">A [*surfaced shadow copy*](vssgloss-s.md) is one in which the shadow copy is known to a system's Mount Manager namespace.</span></span>

<span data-ttu-id="df106-124">Cela signifie que vous pouvez localiser ces clichés instantanés comme vous le feriez pour tout autre volume disponible mais pas encore monté, en utilisant **FindFirstVolume** et **FindNextVolume**, par exemple.</span><span class="sxs-lookup"><span data-stu-id="df106-124">This means that you can locate such shadow copies just as you would locate any other available but not-yet-mounted volume—by using **FindFirstVolume** and **FindNextVolume**, for example.</span></span>

<span data-ttu-id="df106-125">En clair, les clichés instantanés exposés sont également des clichés instantanés en surface.</span><span class="sxs-lookup"><span data-stu-id="df106-125">Clearly, then, exposed shadow copies are also surfaced shadow copies.</span></span> <span data-ttu-id="df106-126">Toutefois, l’inverse n’est pas nécessairement vrai.</span><span class="sxs-lookup"><span data-stu-id="df106-126">However, the reverse is not necessarily true.</span></span>

<span data-ttu-id="df106-127">Si un cliché instantané exposé localement a été démonté, ou si un système a choisi de déconnecter un cliché instantané exposé à distance, ce cliché instantané n’est plus exposé.</span><span class="sxs-lookup"><span data-stu-id="df106-127">If a locally exposed shadow copy was dismounted, or a system chose to disconnect a remotely exposed shadow copy, that shadow copy would no longer be exposed.</span></span> <span data-ttu-id="df106-128">Toutefois, tant que le cliché instantané est rendu persistant, les volumes sont exposés.</span><span class="sxs-lookup"><span data-stu-id="df106-128">However, as long as the shadow copy persisted, the volumes would be surfaced.</span></span> <span data-ttu-id="df106-129">Cela signifie qu’elles peuvent être montées comme tout autre volume en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="df106-129">This means they could be mounted like any other read-only volume.</span></span>

 

 



