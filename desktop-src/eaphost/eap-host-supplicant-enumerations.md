---
title: Énumérations du demandeur EAPHost
description: En savoir plus sur les énumérations de l’API Supplier EAPHost, telles que EapHostPeerMethodResultReason et l’état d’isolement \_ .
ms.assetid: ba4d5a7f-3a5d-4ca3-975e-1ffa182b9014
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e214682a9b94c98db5981a0df8c2b8619814f1e5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103842714"
---
# <a name="eaphost-supplicant-enumerations"></a><span data-ttu-id="2c830-103">Énumérations du demandeur EAPHost</span><span class="sxs-lookup"><span data-stu-id="2c830-103">EAPHost Supplicant Enumerations</span></span>

<span data-ttu-id="2c830-104">Les énumérations de l’API du demandeur EAPHost sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="2c830-104">The EAPHost Supplicant API enumerations are as follows.</span></span>



| <span data-ttu-id="2c830-105">Énumération</span><span class="sxs-lookup"><span data-stu-id="2c830-105">Enumeration</span></span>                                                                  | <span data-ttu-id="2c830-106">Description</span><span class="sxs-lookup"><span data-stu-id="2c830-106">Description</span></span>                                                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2c830-107">**\_type de \_ données de l’interface utilisateur interactive EAP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2c830-107">**EAP\_INTERACTIVE\_UI\_DATA\_TYPE**</span></span>](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type)     | <span data-ttu-id="2c830-108">Spécifie le jeu de types de données de contexte d’interface utilisateur interactif fourni à certains appels d’API demandeur.</span><span class="sxs-lookup"><span data-stu-id="2c830-108">Specifies the set of types of interactive user interface context data supplied to certain supplicant API calls.</span></span>    |
| [<span data-ttu-id="2c830-109">**TYPE de propriété de la \_ méthode EAP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2c830-109">**EAP\_METHOD\_PROPERTY\_TYPE**</span></span>](/windows/desktop/api/EapTypes/ne-eaptypes-eap_method_property_type)              | <span data-ttu-id="2c830-110">Windows 7 ou version ultérieure : spécifie le type de propriété de la méthode.</span><span class="sxs-lookup"><span data-stu-id="2c830-110">Windows 7 or later: Specifies the method property type.</span></span>                                                            |
| [<span data-ttu-id="2c830-111">**\_type de \_ valeur de propriété \_ \_ de la méthode EAP**</span><span class="sxs-lookup"><span data-stu-id="2c830-111">**EAP\_METHOD\_PROPERTY\_VALUE\_TYPE**</span></span>](/windows/desktop/api/EapTypes/ne-eaptypes-eap_method_property_value_type) | <span data-ttu-id="2c830-112">Windows 7 ou version ultérieure : spécifie le type de données d’une valeur de propriété de méthode.</span><span class="sxs-lookup"><span data-stu-id="2c830-112">Windows 7 or later: Specifies the data type of a method property value.</span></span>                                            |
| [<span data-ttu-id="2c830-113">**\_État d’authentification EAPHOST \_**</span><span class="sxs-lookup"><span data-stu-id="2c830-113">**EAPHOST\_AUTH\_STATUS**</span></span>](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-eaphost_auth_status)                         | <span data-ttu-id="2c830-114">Définit l’ensemble des valeurs possibles d’état de session d’authentification EAP.</span><span class="sxs-lookup"><span data-stu-id="2c830-114">Defines the set of possible EAP authentication session status values.</span></span>                                              |
| [<span data-ttu-id="2c830-115">**EapHostPeerAuthParams**</span><span class="sxs-lookup"><span data-stu-id="2c830-115">**EapHostPeerAuthParams**</span></span>](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerauthparams)                       | <span data-ttu-id="2c830-116">Définit l’ensemble des valeurs de paramètre d’authentification possibles.</span><span class="sxs-lookup"><span data-stu-id="2c830-116">Defines the set of possible authentication parameter values.</span></span>                                                       |
| [<span data-ttu-id="2c830-117">**EapHostPeerMethodResultReason**</span><span class="sxs-lookup"><span data-stu-id="2c830-117">**EapHostPeerMethodResultReason**</span></span>](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeermethodresultreason)       | <span data-ttu-id="2c830-118">Définit l’ensemble des raisons possibles qui décrivent les résultats retournés par une méthode EAP à un demandeur.</span><span class="sxs-lookup"><span data-stu-id="2c830-118">Defines the set of possible reasons that describe the results returned by an EAP method to a supplicant.</span></span>           |
| [<span data-ttu-id="2c830-119">**EapHostPeerResponseAction**</span><span class="sxs-lookup"><span data-stu-id="2c830-119">**EapHostPeerResponseAction**</span></span>](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction)               | <span data-ttu-id="2c830-120">Définit l’ensemble d’actions qu’un authentificateur ou une méthode homologue EAP peut indiquer à un demandeur pendant l’authentification.</span><span class="sxs-lookup"><span data-stu-id="2c830-120">Defines the set of actions an EAP authenticator or peer method can indicate to a supplicant during authentication.</span></span> |
| [<span data-ttu-id="2c830-121">**État d’isolement \_**</span><span class="sxs-lookup"><span data-stu-id="2c830-121">**ISOLATION\_STATE**</span></span>](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state)                                  | <span data-ttu-id="2c830-122">Définit l’ensemble des valeurs d’état d’isolement possibles d’un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="2c830-122">Defines the set of possible isolation status values of a machine.</span></span>                                                  |



 

 

 




