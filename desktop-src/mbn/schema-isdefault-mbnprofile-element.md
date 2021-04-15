---
description: Spécifie s’il s’agit du profil par défaut pour l’appareil.
ms.assetid: 024ef936-ddf4-41f6-81c9-5c8a632690a0
title: Élément IsDefault (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsDefault
api_type:
- Schema
ms.openlocfilehash: a59001e385fa7007d188daf2c1348d1a00c3a074
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484825"
---
# <a name="isdefault-mbnprofile-element"></a><span data-ttu-id="afb22-103">Élément IsDefault (MBNProfile)</span><span class="sxs-lookup"><span data-stu-id="afb22-103">IsDefault (MBNProfile) Element</span></span>

<span data-ttu-id="afb22-104">L’élément **IsDefault (MBNProfile)** spécifie s’il s’agit du profil par défaut pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="afb22-104">The **IsDefault (MBNProfile)** element specifies if this is the default profile for the device.</span></span>

<span data-ttu-id="afb22-105">Il s’agit d’un élément facultatif et, s’il n’est pas spécifié, le profil n’est pas défini comme profil par défaut.</span><span class="sxs-lookup"><span data-stu-id="afb22-105">This is an optional element and if it is not specified then the profile will not be set as the default profile.</span></span>

<span data-ttu-id="afb22-106">Le profil par défaut est utilisé par le service haut débit mobile pour les besoins suivants :</span><span class="sxs-lookup"><span data-stu-id="afb22-106">The default profile is used by the Mobile Broadband service for following purposes</span></span>

-   <span data-ttu-id="afb22-107">Le service haut débit mobile utilise les paramètres de connexion du profil par défaut lors de l’exécution de connexions réseau automatiques.</span><span class="sxs-lookup"><span data-stu-id="afb22-107">The Mobile Broadband service uses connection settings from the default profile when performing automatic network connections.</span></span> <span data-ttu-id="afb22-108">Ces paramètres incluent le nom du point d’accès, le nom d’utilisateur, le mot de passe, etc.</span><span class="sxs-lookup"><span data-stu-id="afb22-108">These settings include access point name, user name, password, etc.</span></span>
-   <span data-ttu-id="afb22-109">La stratégie de connexion automatique pour un appareil haut débit mobile est tirée de son profil par défaut.</span><span class="sxs-lookup"><span data-stu-id="afb22-109">Auto connection policy for a Mobile Broadband device is taken from it's default profile.</span></span>
-   <span data-ttu-id="afb22-110">L’interface utilisateur de la connexion réseau du système d’exploitation utilise également les données de connexion du profil par défaut pour les opérations de connexion.</span><span class="sxs-lookup"><span data-stu-id="afb22-110">The operating system network connection UI also uses connection data from the default profile for connection operations.</span></span>

<span data-ttu-id="afb22-111">Les fournisseurs de services mobiles peuvent fournir les détails de connexion dans un profil et configurer ce profil comme profil par défaut.</span><span class="sxs-lookup"><span data-stu-id="afb22-111">Cellular service providers can provide the connection details in a profile and configure that profile as a default profile.</span></span> <span data-ttu-id="afb22-112">Le service haut débit mobile utilise ces paramètres de connexion sans inviter l’utilisateur à entrer des détails.</span><span class="sxs-lookup"><span data-stu-id="afb22-112">The Mobile Broadband service will use these connection settings without prompting user for details.</span></span>

``` syntax
<xs:element name="IsDefault"
    type="boolean"
 />
```

<span data-ttu-id="afb22-113">L’élément **IsDefault** est défini par l’élément [**MBNProfile**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="afb22-113">The **IsDefault** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="afb22-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="afb22-114">Requirements</span></span>



| <span data-ttu-id="afb22-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="afb22-115">Requirement</span></span> | <span data-ttu-id="afb22-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="afb22-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="afb22-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="afb22-117">Minimum supported client</span></span><br/> | <span data-ttu-id="afb22-118">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="afb22-118">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="afb22-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="afb22-119">Minimum supported server</span></span><br/> | <span data-ttu-id="afb22-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="afb22-120">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="afb22-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="afb22-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="afb22-122">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="afb22-122">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="afb22-123">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="afb22-123">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="afb22-124">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="afb22-124">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="afb22-125">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="afb22-125">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




