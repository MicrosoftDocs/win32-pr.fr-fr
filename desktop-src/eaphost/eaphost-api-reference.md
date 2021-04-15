---
title: Informations de référence sur l’API EAPHost
description: En savoir plus sur les API EAPHost et leurs composants. Consultez les informations de référence pour les différentes rubriques d’API, comme le schéma XML EAPHost.
ms.assetid: ac2f074f-b525-42a2-8637-c96a08d77714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6c4d80c402f963a05bbcfb79ca451541603489e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382828"
---
# <a name="eaphost-api-reference"></a><span data-ttu-id="df8da-104">Informations de référence sur l’API EAPHost</span><span class="sxs-lookup"><span data-stu-id="df8da-104">EAPHost API Reference</span></span>

<span data-ttu-id="df8da-105">Les API EAPHost sont divisées en trois composants : les API du demandeur, qui peuvent être directement appelées à partir d’une application compatible EAP. les API de méthode d’homologue EAP, qui gèrent les demandes des demandeurs pour un type d’authentification EAP spécifique et déclenchent des éléments interactifs sur le client ; et les API de l’authentificateur EAP, qui effectuent l’authentification côté serveur d’un demandeur.</span><span class="sxs-lookup"><span data-stu-id="df8da-105">The EAPHost APIs are divided into three components: the supplicant APIs, which are directly callable from an EAP-enabled application; the EAP peer method APIs, which manage supplicant requests for a specific EAP authentication type and raise interactive elements on the client; and the EAP authenticator APIS, which perform the server-side authentication of a supplicant.</span></span>

<span data-ttu-id="df8da-106">Les deux derniers composants d’API, à la méthode d’homologue EAP et aux API de méthode d’authentificateur EAP, requièrent une implémentation personnalisée et conforme dans des dll qui les exposent au service EAPHost.</span><span class="sxs-lookup"><span data-stu-id="df8da-106">The latter two API components -- the EAP Peer Method and EAP Authenticator Method APIs -- require custom and conformant implementation in DLLs that expose them to the EAPHost service.</span></span> <span data-ttu-id="df8da-107">Elles ne peuvent pas être appelées directement à partir du code d’application ; au lieu de cela, elles sont appelées par EAPHost (côté client pour les méthodes homologues EAP et côté serveur pour les méthodes d’authentificateur EAP) si l’implémentation correspond aux signatures d’API spécifiées dans la documentation correspondante.</span><span class="sxs-lookup"><span data-stu-id="df8da-107">They cannot be called directly from application code; instead, they are called by EAPHost (on client side for EAP peer methods, and on the server side for EAP authenticator methods) if the implementation matches the API signatures specified in the corresponding documentation.</span></span> <span data-ttu-id="df8da-108">Les informations spécifiques à l’implémentation de l’API sont fournies sur chaque page de référence de fonction.</span><span class="sxs-lookup"><span data-stu-id="df8da-108">API implementation specific information is provided on each function reference page.</span></span>

## <a name="eaphost-registry-settings"></a><span data-ttu-id="df8da-109">Paramètres du Registre EAPHost</span><span class="sxs-lookup"><span data-stu-id="df8da-109">EAPHost Registry Settings</span></span>



| <span data-ttu-id="df8da-110">Rubrique</span><span class="sxs-lookup"><span data-stu-id="df8da-110">Topic</span></span>                                                      | <span data-ttu-id="df8da-111">Description</span><span class="sxs-lookup"><span data-stu-id="df8da-111">Description</span></span>                                      |
|------------------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="df8da-112">Paramètres du Registre EAPHost</span><span class="sxs-lookup"><span data-stu-id="df8da-112">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md) | <span data-ttu-id="df8da-113">Décrit les clés de Registre consommées par EAPHost.</span><span class="sxs-lookup"><span data-stu-id="df8da-113">Describes the registry keys consumed by EAPHost.</span></span> |



 

## <a name="eaphost-xml-schema"></a><span data-ttu-id="df8da-114">Schéma XML EAPHost</span><span class="sxs-lookup"><span data-stu-id="df8da-114">EAPHost XML Schema</span></span>



| <span data-ttu-id="df8da-115">Rubrique</span><span class="sxs-lookup"><span data-stu-id="df8da-115">Topic</span></span>                                            | <span data-ttu-id="df8da-116">Description</span><span class="sxs-lookup"><span data-stu-id="df8da-116">Description</span></span>                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="df8da-117">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="df8da-117">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md) | <span data-ttu-id="df8da-118">Décrit le schéma EAPHost et le schéma hérité pour créer des données XML de configuration et des informations d’identification XML.</span><span class="sxs-lookup"><span data-stu-id="df8da-118">Describes the EAPHost schema and legacy schema for creating configuration XML and credential XML.</span></span> |



 

## <a name="common-eaphost-api-reference"></a><span data-ttu-id="df8da-119">Informations de référence sur les API EAPHost courantes</span><span class="sxs-lookup"><span data-stu-id="df8da-119">Common EAPHost API Reference</span></span>



| <span data-ttu-id="df8da-120">Rubrique</span><span class="sxs-lookup"><span data-stu-id="df8da-120">Topic</span></span>                                                                   | <span data-ttu-id="df8da-121">Description</span><span class="sxs-lookup"><span data-stu-id="df8da-121">Description</span></span>                                  |
|-------------------------------------------------------------------------|----------------------------------------------|
| [<span data-ttu-id="df8da-122">Énumérations d’API EAPHost courantes</span><span class="sxs-lookup"><span data-stu-id="df8da-122">Common EAPHost API Enumerations</span></span>](common-eap-host-api-enumerations.md) | <span data-ttu-id="df8da-123">Répertorie les constantes communes à toutes les API EAPHost.</span><span class="sxs-lookup"><span data-stu-id="df8da-123">Lists constants common to all EAPHost APIs.</span></span>  |
| [<span data-ttu-id="df8da-124">Structures d’API EAPHost courantes</span><span class="sxs-lookup"><span data-stu-id="df8da-124">Common EAPHost API Structures</span></span>](common-eap-host-api-structures.md)     | <span data-ttu-id="df8da-125">Répertorie les structures communes à toutes les API EAPHost.</span><span class="sxs-lookup"><span data-stu-id="df8da-125">Lists structures common to all EAPHost APIs.</span></span> |
| [<span data-ttu-id="df8da-126">Constantes d’API EAPHost courantes</span><span class="sxs-lookup"><span data-stu-id="df8da-126">Common EAPHost API Constants</span></span>](common-eap-host-error-constants.md)     | <span data-ttu-id="df8da-127">Répertorie les constantes communes à toutes les API EAPHost.</span><span class="sxs-lookup"><span data-stu-id="df8da-127">Lists constants common to all EAPHost APIs.</span></span>  |



 

## <a name="eaphost-api-reference"></a><span data-ttu-id="df8da-128">Informations de référence sur l’API EAPHost</span><span class="sxs-lookup"><span data-stu-id="df8da-128">EAPHost API Reference</span></span>



| <span data-ttu-id="df8da-129">Rubrique</span><span class="sxs-lookup"><span data-stu-id="df8da-129">Topic</span></span>                                                                       | <span data-ttu-id="df8da-130">Description</span><span class="sxs-lookup"><span data-stu-id="df8da-130">Description</span></span>                                                                                                                                      |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="df8da-131">Informations de référence sur l’API Supplier EAPHost</span><span class="sxs-lookup"><span data-stu-id="df8da-131">EAPHost Supplicant API Reference</span></span>](eap-host-supplicant-api-reference.md)   | <span data-ttu-id="df8da-132">Décrit les éléments d’API disponibles pour activer les appels de demandeur à EAPHost.</span><span class="sxs-lookup"><span data-stu-id="df8da-132">Describes the API elements available to enable supplicant calls to EAPHost.</span></span>                                                                      |
| [<span data-ttu-id="df8da-133">Informations de référence sur l’API de méthode homologue EAPHost</span><span class="sxs-lookup"><span data-stu-id="df8da-133">EAPHost Peer Method API Reference</span></span>](eap-host-peer-method-api-reference.md) | <span data-ttu-id="df8da-134">Décrit les éléments d’API qui doivent être implémentés pour créer une DLL de méthode homologue EAP qui peut être chargée et appelée par une EAPHost cliente.</span><span class="sxs-lookup"><span data-stu-id="df8da-134">Describes the API elements that must be implemented to create an EAP peer method DLL that can be loaded and called by a client EAPHost.</span></span>          |
| [<span data-ttu-id="df8da-135">API de méthode d’authentificateur EAPHost</span><span class="sxs-lookup"><span data-stu-id="df8da-135">EAPHost Authenticator Method APIs</span></span>](eaphost-authenticator-method-apis.md)  | <span data-ttu-id="df8da-136">Décrit les éléments d’API qui doivent être implémentés pour créer une DLL de méthode d’authentificateur EAP qui peut être chargée et appelée par un serveur EAPHost.</span><span class="sxs-lookup"><span data-stu-id="df8da-136">Describes the API elements that must be implemented to create an EAP authenticator method DLL that can be loaded and called by a server EAPHost.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="df8da-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="df8da-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df8da-138">À propos d’EAPHost</span><span class="sxs-lookup"><span data-stu-id="df8da-138">About EAPHost</span></span>](about-eap-host.md)
</dt> <dt>

[<span data-ttu-id="df8da-139">Utilisation d’EAPHost</span><span class="sxs-lookup"><span data-stu-id="df8da-139">Using EAPHost</span></span>](using-eap-host.md)
</dt> </dl>

 

 




