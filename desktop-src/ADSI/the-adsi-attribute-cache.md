---
title: Le cache des attributs ADSI
description: Le modèle d’objet ADSI fournit un cache d’attributs côté client pour chaque objet ADSI.
ms.assetid: 0d2b4117-11f2-4b39-8fe5-3b176e4256f4
ms.tgt_platform: multiple
keywords:
- ADSI du cache des attributs ADSI
- ADSI ADSI, utilisation, accès et manipulation des données avec ADSI, cache d’attributs
- attributs ADSI, mise en cache des attributs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df3062ed5862f11e9db5dadd83b80ac624218c81
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671117"
---
# <a name="the-adsi-attribute-cache"></a><span data-ttu-id="f1648-106">Le cache des attributs ADSI</span><span class="sxs-lookup"><span data-stu-id="f1648-106">The ADSI Attribute Cache</span></span>

<span data-ttu-id="f1648-107">Le modèle d’objet ADSI fournit un cache d’attributs côté client pour chaque objet ADSI.</span><span class="sxs-lookup"><span data-stu-id="f1648-107">The ADSI object model provides a client-side attribute cache for each ADSI object.</span></span> <span data-ttu-id="f1648-108">Le cache des attributs est comparable à une table en mémoire qui contient les noms et les valeurs de la plupart des attributs d’objet qui ont été téléchargés.</span><span class="sxs-lookup"><span data-stu-id="f1648-108">The attribute cache is comparable to a table in memory that contains the names and values of most object attributes that have been downloaded.</span></span> <span data-ttu-id="f1648-109">Certains attributs, tels que les attributs opérationnels, ne sont pas mis en cache.</span><span class="sxs-lookup"><span data-stu-id="f1648-109">Some attributes, such as operational attributes, are not cached.</span></span> <span data-ttu-id="f1648-110">ADSI utilise la mise en cache de propriété pour améliorer les performances de manipulation d’attributs et ajouter une fonctionnalité de transaction pour les opérations de lecture et d’écriture d’attributs.</span><span class="sxs-lookup"><span data-stu-id="f1648-110">ADSI uses property caching to enhance the performance of attribute manipulation and add transactioning capability for attribute read and write operations.</span></span> <span data-ttu-id="f1648-111">Cette fonctionnalité est essentielle pour les clients écrits dans des langages qui n’ont pas de mécanisme de traitement par lot natif pour définir des attributs, tels que le système de développement Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f1648-111">This capability is critical for clients written in languages that have no native batching mechanism for setting attributes, such as Microsoft Visual Basic development system.</span></span> <span data-ttu-id="f1648-112">Sans le cache de propriété ADSI, ces clients doivent accéder au serveur chaque fois qu’un attribut est lu ou écrit.</span><span class="sxs-lookup"><span data-stu-id="f1648-112">Without the ADSI property cache, such clients would have to access the server every time an attribute is read or written.</span></span>

<span data-ttu-id="f1648-113">Lorsqu’un objet est créé ou lié pour la première fois à, le cache de propriétés de l’objet est vide.</span><span class="sxs-lookup"><span data-stu-id="f1648-113">When an object is created or first bound to, the property cache for the object is empty.</span></span> <span data-ttu-id="f1648-114">Lorsque la méthode [**IADs :: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) est appelée, ADSI charge les attributs demandés pour l’objet à partir du service d’annuaire sous-jacent dans le cache local.</span><span class="sxs-lookup"><span data-stu-id="f1648-114">When the [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) method is called, ADSI loads the requested attributes for the object from the underlying directory service into the local cache.</span></span> <span data-ttu-id="f1648-115">Lorsqu’une valeur d’attribut spécifique est lue et que le cache est vide, ADSI effectue un appel implicite à la méthode **IADs :: GetInfo** .</span><span class="sxs-lookup"><span data-stu-id="f1648-115">When a specific attribute value is read and the cache is empty, ADSI makes an implicit call to the **IADs::GetInfo** method.</span></span> <span data-ttu-id="f1648-116">Lorsque le cache est rempli, toutes les opérations de lecture d’attribut fonctionnent uniquement sur le contenu du cache.</span><span class="sxs-lookup"><span data-stu-id="f1648-116">When the cache is filled, all attribute read operations work on the contents of the cache only.</span></span>

<span data-ttu-id="f1648-117">Lorsqu’une valeur d’attribut est écrite, la nouvelle valeur est stockée dans le cache local jusqu’à ce que la méthode [**IADs :: setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) soit appelée.</span><span class="sxs-lookup"><span data-stu-id="f1648-117">When an attribute value is written, the new value is stored in the local cache until the [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method is called.</span></span> <span data-ttu-id="f1648-118">Lorsque la méthode **IADs :: setinfo** est appelée, les attributs du cache sont validés dans le service d’annuaire sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="f1648-118">When the **IADs::SetInfo** method is called, the attributes in the cache are committed to the underlying directory service.</span></span> <span data-ttu-id="f1648-119">Après l’appel de la méthode **IADs :: setinfo** , les valeurs restent dans le cache jusqu’à ce qu’elles soient explicitement actualisées avec un autre appel à la méthode [**IADs :: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) .</span><span class="sxs-lookup"><span data-stu-id="f1648-119">After the **IADs::SetInfo** method is called, the values remain in the cache until explicitly refreshed with another call to the [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f1648-120">La méthode [**IADs :: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) doit être utilisée avec précaution, car cette méthode remplacera toujours les valeurs d’attribut dans le cache à partir du service d’annuaire sous-jacent, même si la valeur mise en cache a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="f1648-120">The [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) method must be used carefully because this method will always overwrite the attribute values in the cache from the underlying directory service, even if the cached value has been changed.</span></span> <span data-ttu-id="f1648-121">Autrement dit, elle remplacera les valeurs d’attribut qui ont été modifiées dans le cache, mais non validées dans le service d’annuaire sous-jacent avec un appel à la méthode [**IADs :: setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .</span><span class="sxs-lookup"><span data-stu-id="f1648-121">That is, it will overwrite attribute values that have been changed in the cache, but not committed to the underlying directory service with a call to the [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method.</span></span>

 

<span data-ttu-id="f1648-122">L’illustration suivante montre les différentes méthodes utilisées pour fonctionner sur le cache.</span><span class="sxs-lookup"><span data-stu-id="f1648-122">The following figure shows the different methods used to operate on the cache.</span></span>

![cache d’attributs ADSI](images/ds2propc.png)

 

 




