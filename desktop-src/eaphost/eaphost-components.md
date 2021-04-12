---
title: Composants d’EAPHost
description: En savoir plus sur les trois composants de l’authentification EAPHost. Affichez les ressources disponibles supplémentaires pour l’utilisation de l’authentification EAPHost.
ms.assetid: f875c3f8-d2fb-461e-b356-e1b2ccaf9981
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ede2fc6a705ec77fe982778239a92c7ffb10ef9
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463718"
---
# <a name="components-of-eaphost"></a><span data-ttu-id="dab4f-104">Composants d’EAPHost</span><span class="sxs-lookup"><span data-stu-id="dab4f-104">Components of EAPHost</span></span>

<span data-ttu-id="dab4f-105">Cette rubrique décrit les trois composants de l’authentification EAPHost.</span><span class="sxs-lookup"><span data-stu-id="dab4f-105">This topic describes the three components of EAPHost authentication.</span></span>

## <a name="eaphost-components"></a><span data-ttu-id="dab4f-106">Composants EAPHost</span><span class="sxs-lookup"><span data-stu-id="dab4f-106">EAPHost Components</span></span>

<span data-ttu-id="dab4f-107">L’authentification EAPHost comporte les trois composants suivants.</span><span class="sxs-lookup"><span data-stu-id="dab4f-107">EAPHost authentication has the following three components.</span></span>

-   <span data-ttu-id="dab4f-108">Le demandeur, qui effectue les demandes d’authentification.</span><span class="sxs-lookup"><span data-stu-id="dab4f-108">The supplicant, which makes the authentication requests.</span></span>
-   <span data-ttu-id="dab4f-109">Les méthodes EAP homologue (ou client), qui implémentent les méthodes EAP spécifiques et gèrent la session d’authentification côté client.</span><span class="sxs-lookup"><span data-stu-id="dab4f-109">The peer (or client) EAP methods, which implement the specific EAP methods and manage the authentication session on the client side.</span></span>
-   <span data-ttu-id="dab4f-110">Les méthodes EAP de l’authentificateur (ou du serveur) qui implémentent le côté serveur du protocole EAP.</span><span class="sxs-lookup"><span data-stu-id="dab4f-110">The authenticator (or server) EAP methods, which implement the server side of the EAP protocol.</span></span>

<span data-ttu-id="dab4f-111">Les API du demandeur sont appelées directement à partir d’une application qui souhaite s’authentifier via EAPHost.</span><span class="sxs-lookup"><span data-stu-id="dab4f-111">The supplicant APIs are called directly from an application that wants to authenticate via EAPHost.</span></span> <span data-ttu-id="dab4f-112">Toutefois, les API de méthode d’homologue et de méthode d’authentificateur sont des prototypes de fonction qui doivent être implémentés pour un type de méthode d’authentification EAP spécifique, tel que MS-CHAPv2 (Microsoft Challenge Handshake Authentication Protocol version 2,0).</span><span class="sxs-lookup"><span data-stu-id="dab4f-112">The peer method and authenticator method APIs, however, are function prototypes that must be implemented for a specific EAP authentication method type - such as the Microsoft Challenge Handshake Authentication Protocol version 2.0 (MS-CHAPv2).</span></span>

<span data-ttu-id="dab4f-113">Si vous créez une application qui utilisera EAPHost pour l’authentification, reportez-vous à la référence de l' [API du demandeur EAPHost](eap-host-supplicant-api-reference.md).</span><span class="sxs-lookup"><span data-stu-id="dab4f-113">If you are authoring an application that will use EAPHost for authentication, please refer to the [EAPHost Supplicant API Reference](eap-host-supplicant-api-reference.md).</span></span>

<span data-ttu-id="dab4f-114">Si vous créez une nouvelle méthode d’authentification EAP à gérer par EAPHost, reportez-vous à la référence de l' [API de méthode homologue EAPHost](eap-host-peer-method-api-reference.md) et aux [API de méthode d’authentificateur EAPHost](eaphost-authenticator-method-apis.md).</span><span class="sxs-lookup"><span data-stu-id="dab4f-114">If you are authoring a new EAP authentication method to be managed by EAPHost, please refer to the [EAPHost Peer Method API Reference](eap-host-peer-method-api-reference.md) and the [EAPHost Authenticator Method APIs](eaphost-authenticator-method-apis.md).</span></span> <span data-ttu-id="dab4f-115">Notez que vous allez créer des implémentations de ces API exposées dans une nouvelle DLL que EAPHost charge, au lieu de les appeler directement.</span><span class="sxs-lookup"><span data-stu-id="dab4f-115">Note that you will be creating implementations of these APIs exposed in a new DLL that EAPHost loads, rather than calling them directly.</span></span>

 

 




