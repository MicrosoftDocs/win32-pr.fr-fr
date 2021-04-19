---
description: Définit un profil haut débit mobile.
ms.assetid: bfec0a1d-de17-4ebd-b9fb-570e230da317
title: Référence du schéma de profil haut débit mobile
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 425db1d38002e40969bb47c03952330dd6ccd26d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515476"
---
# <a name="mobile-broadband-profile-schema-reference"></a><span data-ttu-id="c982a-103">Référence du schéma de profil haut débit mobile</span><span class="sxs-lookup"><span data-stu-id="c982a-103">Mobile Broadband Profile Schema Reference</span></span>

<span data-ttu-id="c982a-104">Le schéma de profil haut débit mobile définit un profil haut débit mobile.</span><span class="sxs-lookup"><span data-stu-id="c982a-104">The Mobile Broadband Profile Schema defines a Mobile Broadband Profile.</span></span>

<span data-ttu-id="c982a-105">Les profils stockent les paramètres de configuration réseau et d’utilisateur liés à la connexion haut débit mobile.</span><span class="sxs-lookup"><span data-stu-id="c982a-105">Profiles store Mobile Broadband connection related user and network configuration parameters.</span></span> <span data-ttu-id="c982a-106">Ils stockent également les préférences utilisateur pour une connexion.</span><span class="sxs-lookup"><span data-stu-id="c982a-106">They also store the user preferences for a connection.</span></span>

<span data-ttu-id="c982a-107">L’élément racine d’un profil haut débit mobile est l’élément [**MBNProfile**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="c982a-107">The root element of a Mobile Broadband profile is the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span> <span data-ttu-id="c982a-108">Chaque profil a un seul élément racine.</span><span class="sxs-lookup"><span data-stu-id="c982a-108">Each profile has exactly one root element.</span></span> <span data-ttu-id="c982a-109">Tous les éléments de schéma de profil de haut débit mobile utilisés par Windows 7 se trouvent dans l’espace de noms `https://www.microsoft.com/networking/WWAN/profile/v1` et les éléments utilisés par Windows 8 se trouvent dans l’espace de noms `https://www.microsoft.com/networking/WWAN/profile/v2` .</span><span class="sxs-lookup"><span data-stu-id="c982a-109">All Mobile Broadband Profile Schema elements used by Windows 7 are in the namespace `https://www.microsoft.com/networking/WWAN/profile/v1` and the elements used by Windows 8 are in the namespace `https://www.microsoft.com/networking/WWAN/profile/v2`.</span></span>

<span data-ttu-id="c982a-110">Le schéma de profil haut débit mobile impose strictement l’ordre des nœuds.</span><span class="sxs-lookup"><span data-stu-id="c982a-110">The Mobile Broadband Profile Schema strictly enforces the order of the nodes.</span></span> <span data-ttu-id="c982a-111">Les nœuds spécifiés dans un profil doivent adhérer au **schéma de profil haut débit mobile** et s’afficher dans l’ordre indiqué dans la définition de schéma.</span><span class="sxs-lookup"><span data-stu-id="c982a-111">Nodes specified in a profile must adhere to the **Mobile Broadband Profile Schema** and appear in the order prescribed in the schema definition.</span></span> <span data-ttu-id="c982a-112">Par exemple, [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) doit être spécifié immédiatement après [**AccessString**](schema-accessstring-contexttype-element.md).</span><span class="sxs-lookup"><span data-stu-id="c982a-112">For example, [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) must be specified immediately after [**AccessString**](schema-accessstring-contexttype-element.md).</span></span>

-   [<span data-ttu-id="c982a-113">Schéma de profil de haut débit mobile v1</span><span class="sxs-lookup"><span data-stu-id="c982a-113">Mobile Broadband Profile Schema v1</span></span>](mobile-broadband-profile-schema.md)
-   [<span data-ttu-id="c982a-114">Schéma de profil haut débit mobile v2</span><span class="sxs-lookup"><span data-stu-id="c982a-114">Mobile Broadband Profile Schema v2</span></span>](mobile-broadband-profile-schema-v2.md)
-   [<span data-ttu-id="c982a-115">Schéma de profil haut débit mobile v3</span><span class="sxs-lookup"><span data-stu-id="c982a-115">Mobile Broadband Profile Schema v3</span></span>](mobile-broadband-profile-schema-v3.md)
-   <span data-ttu-id="c982a-116">[V4 de schéma de profil haut débit mobile](/previous-versions/windows/desktop/legacy/mt243438(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c982a-116">[Mobile Broadband Profile Schema v4](/previous-versions/windows/desktop/legacy/mt243438(v=vs.85))</span></span>

 

 
