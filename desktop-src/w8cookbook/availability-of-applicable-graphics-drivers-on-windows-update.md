---
title: Disponibilité des pilotes graphiques applicables sur Windows Update
description: La disponibilité de ces pilotes sur Windows Update (WU) détermine si un utilisateur est automatiquement invité à effectuer une mise à niveau de Windows 7, Windows 8 ou Windows 8.1 vers Windows 10.
ms.assetid: 166C0FE3-CB9D-4895-91AC-6E57EC1D8B21
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 208e984199c8de63dfa49133a255865035c84bdd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106513463"
---
# <a name="availability-of-applicable-graphics-drivers-on-windows-update"></a><span data-ttu-id="f4806-103">Disponibilité des pilotes graphiques applicables sur Windows Update</span><span class="sxs-lookup"><span data-stu-id="f4806-103">Availability of applicable graphics drivers on Windows Update</span></span>

<span data-ttu-id="f4806-104">La disponibilité de ces pilotes sur Windows Update (WU) détermine si un utilisateur est automatiquement invité à effectuer une mise à niveau de Windows 7, Windows 8 ou Windows 8.1 vers Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f4806-104">The availability of these drivers on Windows Update (WU) will determine whether a user is automatically offered an upgrade from Windows 7, Windows 8 or Windows 8.1 to Windows 10.</span></span> <span data-ttu-id="f4806-105">Si des analyses matérielles ont montré qu’aucun pilote graphique n’était disponible sur Windows Update pour la carte graphique du PC, les utilisateurs n’ont pas fourni le système d’exploitation Windows 10 mis à jour.</span><span class="sxs-lookup"><span data-stu-id="f4806-105">If hardware scans showed that there was no graphics driver available on Windows Update for the graphics adapter in the PC, users were not offered the updated Windows 10 OS.</span></span> <span data-ttu-id="f4806-106">Toutefois, les utilisateurs peuvent toujours obtenir Windows 10 par le biais d’autres sources et effectuer manuellement la mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="f4806-106">However, users can still obtain Windows 10 through other sources and manually perform the upgrade.</span></span>

<span data-ttu-id="f4806-107">Certains utilisateurs n’ont pas été sûrs de la raison pour laquelle ils n’ont pas été mis à niveau lorsque d’autres personnes étaient, même si le conseiller de mise à niveau a expliqué qu’aucun pilote graphique n’était disponible pour leur matériel.</span><span class="sxs-lookup"><span data-stu-id="f4806-107">Some users were unsure of why they were not offered the upgrade when other people were, even though the Upgrade Advisor explained that there was no graphics driver available for their hardware.</span></span>

<span data-ttu-id="f4806-108">En outre, certains utilisateurs ont forcé une mise à niveau, puis ont découvert que leurs fonctionnalités graphiques et leurs performances ont été ralenties en raison de l’absence de pilote matériel.</span><span class="sxs-lookup"><span data-stu-id="f4806-108">Additionally, some users forced an upgrade and then found that their graphics functionality and performance suffered due to the lack of a hardware driver.</span></span>

## <a name="mitigations"></a><span data-ttu-id="f4806-109">Corrections</span><span class="sxs-lookup"><span data-stu-id="f4806-109">Mitigations</span></span>

<span data-ttu-id="f4806-110">Pour atténuer ce risque, les utilisateurs peuvent installer manuellement un ancien pilote, c.-à-d. à partir de Windows 7, Windows 8 ou Windows 8.1, en accédant au site Web IHV ou OEM et en téléchargeant un pilote de manière explicite.</span><span class="sxs-lookup"><span data-stu-id="f4806-110">To mitigate this, users can manually install an older driver, i.e. from Windows 7, Windows 8 or Windows 8.1, by going to the IHV or OEM web site and downloading a driver explicitly.</span></span> <span data-ttu-id="f4806-111">Cette opération doit être effectuée après la mise à niveau et n’est pas garantie.</span><span class="sxs-lookup"><span data-stu-id="f4806-111">This must be done after the upgrade and is not guaranteed to work.</span></span> <span data-ttu-id="f4806-112">Aucune solution n’est prise en charge si aucun pilote graphique approprié n’est disponible sur WU.</span><span class="sxs-lookup"><span data-stu-id="f4806-112">There is no supported solution if a suitable graphics driver is not available on WU.</span></span> <span data-ttu-id="f4806-113">L’utilisateur doit décider s’il faut :</span><span class="sxs-lookup"><span data-stu-id="f4806-113">The user must decide whether to:</span></span>

-   <span data-ttu-id="f4806-114">Rester sur le système d’exploitation précédent ;</span><span class="sxs-lookup"><span data-stu-id="f4806-114">Remain on the previous OS;</span></span>
-   <span data-ttu-id="f4806-115">Accepter les limitations du pilote logiciel, carte d’affichage de base Microsoft (MSBDA); ni</span><span class="sxs-lookup"><span data-stu-id="f4806-115">Accept the limitations of the software driver, Microsoft Basic Display Adapter (MSBDA); or</span></span>
-   <span data-ttu-id="f4806-116">Achetez une nouvelle carte graphique disposant d’un pilote Windows 10 pris en charge.</span><span class="sxs-lookup"><span data-stu-id="f4806-116">Buy a new graphics card that has a supported Windows 10 driver.</span></span>

## <a name="solutions"></a><span data-ttu-id="f4806-117">Solutions</span><span class="sxs-lookup"><span data-stu-id="f4806-117">Solutions</span></span>

<span data-ttu-id="f4806-118">Il est essentiel que les IHV et les OEM chargent leurs pilotes graphiques Windows 10 dans WU pour tout matériel qu’ils envisagent de prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="f4806-118">It’s critical that IHVs and OEMs upload their Windows 10 graphics drivers to WU for any hardware that they intend to support.</span></span>

<span data-ttu-id="f4806-119">Notez que le matériel qui a atteint la fin de vie (EOL) peut ne pas avoir de pilotes sur WU.</span><span class="sxs-lookup"><span data-stu-id="f4806-119">Note that hardware that has reached End-Of-Live (EOL) might not have drivers on WU.</span></span> <span data-ttu-id="f4806-120">Il n’existe aucune solution dans ce cas : l’utilisateur doit choisir l’une des options sous atténuations ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="f4806-120">There is no solution in this case – the user must choose one of the options under Mitigations above.</span></span>

 

 




