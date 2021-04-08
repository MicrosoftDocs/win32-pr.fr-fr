---
description: Obtient la version du moteur de traitement WPAD.
ms.assetid: f9e9a867-d491-4d46-bbd8-c0c3d8d5b3d6
title: getClientVersion fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- dnsResolveEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: e0bcf439c8a282e42a28126824ffb70630a341e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866230"
---
# <a name="getclientversion-function"></a><span data-ttu-id="d25de-103">getClientVersion fonction)</span><span class="sxs-lookup"><span data-stu-id="d25de-103">getClientVersion function</span></span>

<span data-ttu-id="d25de-104">Obtient la version du moteur de traitement WPAD.</span><span class="sxs-lookup"><span data-stu-id="d25de-104">Gets the version of the WPAD processing engine.</span></span>

## <a name="parameters"></a><span data-ttu-id="d25de-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d25de-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d25de-106">*IpAddressList*</span><span class="sxs-lookup"><span data-stu-id="d25de-106">*IpAddressList*</span></span> 
</dt> <dd>

<span data-ttu-id="d25de-107">Chaîne délimitée par des points-virgules contenant des adresses IP.</span><span class="sxs-lookup"><span data-stu-id="d25de-107">A semi-colon delimited string containing IP addresses.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d25de-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d25de-108">Return value</span></span>

<span data-ttu-id="d25de-109">Liste d’adresses IP séparées par des points-virgules triées ou une chaîne vide si le tri de la liste d’adresses IP est impossible.</span><span class="sxs-lookup"><span data-stu-id="d25de-109">A list of sorted semi-colon delimited IP addresses or an empty string if unable to sort the IP Address list.</span></span>

## <a name="remarks"></a><span data-ttu-id="d25de-110">Notes</span><span class="sxs-lookup"><span data-stu-id="d25de-110">Remarks</span></span>

<span data-ttu-id="d25de-111">Actuellement, cette fonction retourne la version 1,0.</span><span class="sxs-lookup"><span data-stu-id="d25de-111">Currently this function returns version 1.0.</span></span>

<span data-ttu-id="d25de-112">Microsoft a ajouté cette fonction pour permettre aux administrateurs informatiques de mettre à jour leurs scripts WPAD afin d’utiliser différentes versions du moteur de traitement WPAD sans causer de ruptures au déploiement existant.</span><span class="sxs-lookup"><span data-stu-id="d25de-112">Microsoft added this function to allow IT administrators to update their WPAD scripts to use different versions of the WPAD processing engine without causing breaks to their existing deployment.</span></span> <span data-ttu-id="d25de-113">Par exemple, si Microsoft a ajouté une fonction à la version 2,0 du moteur WPAD, les administrateurs peuvent vérifier la version avant de tenter d’appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="d25de-113">For example, if Microsoft added a function to the 2.0 version of the WPAD engine, then administrators can check the version before attempting to call that function.</span></span> <span data-ttu-id="d25de-114">Cela permet à leur script de fonctionner avec le client exécutant les versions 1,0 et 2,0 du moteur WPAD.</span><span class="sxs-lookup"><span data-stu-id="d25de-114">This allows their script to work with client running versions 1.0 and 2.0 of the WPAD engine.</span></span>

## <a name="examples"></a><span data-ttu-id="d25de-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="d25de-115">Examples</span></span>

``` syntax
getClientVersion();
    returns the appropriate versions number of the WPAD engine.
```

## <a name="see-also"></a><span data-ttu-id="d25de-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d25de-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d25de-117">Définitions d’API d’assistance du proxy compatibles IPv6</span><span class="sxs-lookup"><span data-stu-id="d25de-117">IPv6-Aware Proxy Helper API Definitions</span></span>](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[<span data-ttu-id="d25de-118">Extensions IPv6 du format de fichier de configuration automatique du navigateur</span><span class="sxs-lookup"><span data-stu-id="d25de-118">IPv6 Extensions to Navigator Auto-Config File Format</span></span>](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



