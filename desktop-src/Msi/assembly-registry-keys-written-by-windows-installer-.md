---
description: Si un package Windows Installer installe ou publie des assemblys, le programme d’installation stocke les informations relatives à ces assemblys dans le Registre du système local.
ms.assetid: 1a6b0530-b5ad-49db-bc08-5b20d32420ef
title: Clés de registre de l’assembly écrites par Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bdd2ea7d290659fa9c1578d89be9a77dcc5cc10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528869"
---
# <a name="assembly-registry-keys-written-by-windows-installer"></a><span data-ttu-id="96ce3-103">Clés de registre de l’assembly écrites par Windows Installer</span><span class="sxs-lookup"><span data-stu-id="96ce3-103">Assembly Registry Keys Written by Windows Installer</span></span>

<span data-ttu-id="96ce3-104">Si un package Windows Installer installe ou publie des assemblys, le programme d’installation stocke les informations relatives à ces assemblys dans le Registre du système local.</span><span class="sxs-lookup"><span data-stu-id="96ce3-104">If a Windows Installer package installs or advertises assemblies, the installer stores information about those assemblies in the local system registry.</span></span> <span data-ttu-id="96ce3-105">Notez que ces clés de Registre sont uniquement destinées à être utilisées en interne par Windows Installer et qu’elles ne doivent pas être exploitées par votre application.</span><span class="sxs-lookup"><span data-stu-id="96ce3-105">Please note that these registry keys are only intended to be used internally by Windows Installer and they should not be relied upon by your application.</span></span> <span data-ttu-id="96ce3-106">Le contenu, l’emplacement et la structure des informations stockées dans ces clés sont susceptibles d’être modifiés.</span><span class="sxs-lookup"><span data-stu-id="96ce3-106">The content, location, and structure of information stored in these keys is subject to change.</span></span> <span data-ttu-id="96ce3-107">Les applications doivent s’appuyer sur [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) pour gérer les assemblys.</span><span class="sxs-lookup"><span data-stu-id="96ce3-107">Applications should rely upon [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) to manage assemblies.</span></span>

<span data-ttu-id="96ce3-108">Les assemblys sont inscrits par leurs noms d’assemblys.</span><span class="sxs-lookup"><span data-stu-id="96ce3-108">Assemblies are registered by their assembly names.</span></span> <span data-ttu-id="96ce3-109">Les noms des valeurs stockées dans les emplacements suivants sont les noms d’assemblys.</span><span class="sxs-lookup"><span data-stu-id="96ce3-109">The names of the values stored in the following locations are the assembly names.</span></span> <span data-ttu-id="96ce3-110">Les valeurs réelles sont du type REG \_ multi- \_ SZ et contiennent des données utilisées par [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) pour installer ou réparer des assemblys.</span><span class="sxs-lookup"><span data-stu-id="96ce3-110">The actual values are of the type REG\_MULTI\_SZ and contain data used by [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) to install or repair assemblies.</span></span>

## <a name="information-about-private-assemblies"></a><span data-ttu-id="96ce3-111">Informations sur les assemblys privés</span><span class="sxs-lookup"><span data-stu-id="96ce3-111">Information About Private Assemblies</span></span>

<span data-ttu-id="96ce3-112">Windows Installer stocke les informations sur les assemblys privés transportés par Windows Installer packages qui ont été installés en tant qu’applications gérées par utilisateur sous la clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="96ce3-112">Windows Installer stores information about private assemblies carried by Windows Installer packages that have been installed as managed per-user applications under the following registry key:</span></span>

<span data-ttu-id="96ce3-113">**HKLM** \\ **Logiciel** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Programme d’installation** \\ **Géré** \\ **Sid *_\\_* de l’utilisateur** \\ Chemin d’accès des **assemblys** \\ \* *_du programme d’installation vers le fichier de configuration_* _</span><span class="sxs-lookup"><span data-stu-id="96ce3-113">**HKLM**\\**SOFTWARE**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Installer**\\**Managed**\\**_User SID_*_\\_\* Installer**\\**Assemblies**\\**_path to config file_* _</span></span>

<span data-ttu-id="96ce3-114">Windows Installer stocke les informations sur les assemblys privés transportés par Windows Installer packages qui ont été installés par utilisateur sous la clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="96ce3-114">Windows Installer stores information about private assemblies carried by Windows Installer packages that have been installed per-user under the following registry key:</span></span>

<span data-ttu-id="96ce3-115">_***\\** **\\** **\\** **\\** Chemin d’accès des assemblys du logiciel HKCU Microsoft installer **\\** _vers le fichier de configuration_*_</span><span class="sxs-lookup"><span data-stu-id="96ce3-115">_*HKCU **\\** Software **\\** Microsoft **\\** Installer **\\** Assemblies **\\**_path to config file_*_</span></span>

<span data-ttu-id="96ce3-116">Windows Installer stocke les informations sur les assemblys privés concédés par des packages Windows Installer et installées par ordinateur sous la clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="96ce3-116">Windows Installer stores information about private assemblies carried by Windows Installer packages and installed per-machine under the following registry key:</span></span>

<span data-ttu-id="96ce3-117">_*HKLM **\\** Software **\\** classes **\\** programme **\\** **\\** _d’installation chemin d’accès au fichier de configuration_*_</span><span class="sxs-lookup"><span data-stu-id="96ce3-117">_*HKLM **\\** SOFTWARE **\\** Classes **\\** Installer **\\** Assemblies **\\**_path to config file_*_</span></span>

## <a name="information-about-global-or-shared-assemblies"></a><span data-ttu-id="96ce3-118">Informations sur les assemblys globaux ou partagés</span><span class="sxs-lookup"><span data-stu-id="96ce3-118">Information About Global or Shared Assemblies</span></span>

<span data-ttu-id="96ce3-119">Windows Installer stocke les informations sur les assemblys partagés transportés par Windows Installer packages qui ont été installés en tant qu’applications gérées par utilisateur sous la clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="96ce3-119">Windows Installer stores information about shared assemblies carried by Windows Installer packages that have been installed as managed per-user applications under the following registry key:</span></span>

<span data-ttu-id="96ce3-120">_*HKLM **\\** Logiciel **\\** Microsoft **\\** Windows **\\** CurrentVersion **\\** installer **\\** Managed **\\** _User sid_*_ \\ _ *assemblys de programme d’installation **\\** **\\** Global*\*</span><span class="sxs-lookup"><span data-stu-id="96ce3-120">_*HKLM **\\** SOFTWARE **\\** Microsoft **\\** Windows **\\** CurrentVersion **\\** Installer **\\** Managed **\\**_User SID_*_\\_ *Installer **\\** Assemblies **\\** Global*\*</span></span>

<span data-ttu-id="96ce3-121">Windows Installer stocke les informations sur les assemblys partagés effectués par Windows Installer packages qui ont été installés par utilisateur sous la clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="96ce3-121">Windows Installer stores information about shared assemblies carried by Windows Installer packages that have been installed per-user under the following registry key:</span></span>

<span data-ttu-id="96ce3-122">**HKCU** \\ **Logiciel** \\ **Microsoft** \\ **Programme d’installation** \\ **Assemblys** \\ **Global**</span><span class="sxs-lookup"><span data-stu-id="96ce3-122">**HKCU**\\**Software**\\**Microsoft**\\**Installer**\\**Assemblies**\\**Global**</span></span>

<span data-ttu-id="96ce3-123">Windows Installer stocke les informations sur les assemblys partagés transportés par les packages Windows Installer et installés par ordinateur dans la clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="96ce3-123">Windows Installer stores information about shared assemblies carried by Windows Installer packages and installed per-machine under the following registry key:</span></span>

<span data-ttu-id="96ce3-124">**HKLM** \\ **Logiciel** \\ **Classes** \\ **Programme d’installation** \\ **Assemblys** \\ **Global**</span><span class="sxs-lookup"><span data-stu-id="96ce3-124">**HKLM**\\**SOFTWARE**\\**Classes**\\**Installer**\\**Assemblies**\\**Global**</span></span>

 

 



