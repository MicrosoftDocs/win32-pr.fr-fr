---
description: Chaque identificateur de langue se compose d’un identificateur de langue primaire indiquant la langue et un identificateur de sous-langue indiquant le pays ou la région.
ms.assetid: 8a6373e0-46c2-4b1b-bc67-543f426ef15a
title: Constantes et chaînes de l’identificateur de langue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d80823e897a8325cbcb7207f91bde69397296767
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319393"
---
# <a name="language-identifier-constants-and-strings"></a><span data-ttu-id="b8f71-103">Constantes et chaînes de l’identificateur de langue</span><span class="sxs-lookup"><span data-stu-id="b8f71-103">Language Identifier Constants and Strings</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b8f71-104">Les constantes d’identificateur de langue sont déconseillées et leur utilisation est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="b8f71-104">Language identifier constants are deprecated and their use is discouraged.</span></span> <span data-ttu-id="b8f71-105">L’utilisation de noms de paramètres régionaux au lieu des identificateurs de paramètres régionaux est toujours préférable.</span><span class="sxs-lookup"><span data-stu-id="b8f71-105">Use of locale names instead of locale identifiers is always preferable.</span></span>

<span data-ttu-id="b8f71-106">Pour obtenir une description des identificateurs de langue, consultez [identificateur de langue](language-identifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="b8f71-106">See [language identifier](language-identifiers.md) for a description of language identifiers.</span></span>

<span data-ttu-id="b8f71-107">Un identificateur principal ou de sous-langue peut être défini par l’utilisateur ou prédéfini.</span><span class="sxs-lookup"><span data-stu-id="b8f71-107">A primary or sublanguage identifier can be user-defined or predefined.</span></span> <span data-ttu-id="b8f71-108">Pour obtenir les identificateurs de langue principale prédéfinis avec leurs identificateurs de sous-langue valides, consultez [[MS-LCID] : informations de référence sur l’identificateur LCID (Language code identifier) Windows](/openspecs/windows_protocols/ms-lcid/70feba9f-294e-491e-b6eb-56532684c37f).</span><span class="sxs-lookup"><span data-stu-id="b8f71-108">For the predefined primary language identifiers with their valid sublanguage identifiers, see [[MS-LCID]: Windows Language Code Identifier (LCID) Reference](/openspecs/windows_protocols/ms-lcid/70feba9f-294e-491e-b6eb-56532684c37f).</span></span>

> [!Note]  
> <span data-ttu-id="b8f71-109">S’il n’existe aucun identificateur de sous-langue à utiliser avec un identificateur de langue primaire, votre application doit utiliser la **\_ valeur par défaut de sublang**.</span><span class="sxs-lookup"><span data-stu-id="b8f71-109">If there is no sublanguage identifier to use with a primary language identifier, your application should use **SUBLANG\_DEFAULT**.</span></span> <span data-ttu-id="b8f71-110">Il doit utiliser la sous-langue **\_ neutre** pour les ressources qui sont identiques pour toutes les sous-langues d’une langue primaire.</span><span class="sxs-lookup"><span data-stu-id="b8f71-110">It should use **SUBLANG\_NEUTRAL** for resources that are the same for all sublanguages of a primary language.</span></span>

<span data-ttu-id="b8f71-111">Un identificateur de langue principale défini par l’utilisateur a une valeur comprise dans la plage 0x0200 à 0x03ff.</span><span class="sxs-lookup"><span data-stu-id="b8f71-111">A user-defined primary language identifier has a value in the range 0x0200 to 0x03ff.</span></span> <span data-ttu-id="b8f71-112">Toutes les autres valeurs sont réservées à l’utilisation du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="b8f71-112">All other values are reserved for operating system use.</span></span>

<span data-ttu-id="b8f71-113">Un identificateur de sous-langue défini par l’utilisateur a une valeur comprise dans la plage 0x20 à 0x3F.</span><span class="sxs-lookup"><span data-stu-id="b8f71-113">A user-defined sublanguage identifier has a value in the range 0x20 to 0x3f.</span></span> <span data-ttu-id="b8f71-114">Toutes les autres valeurs sont réservées à l’utilisation du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="b8f71-114">All other values are reserved for operating system use.</span></span>
