---
description: Le transfert est le détournement d’une session entrante vers une adresse de destination différente.
ms.assetid: c70bf596-b2a4-46ec-9b1a-c9d948768b51
title: Transférer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4154e2bb6f8c688feffe2e33d3c5988b0b7da27b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862618"
---
# <a name="forward"></a><span data-ttu-id="1c81d-103">Transférer</span><span class="sxs-lookup"><span data-stu-id="1c81d-103">Forward</span></span>

<span data-ttu-id="1c81d-104">Le transfert est le détournement d’une session entrante vers une adresse de destination différente.</span><span class="sxs-lookup"><span data-stu-id="1c81d-104">Forwarding is the deflection of an incoming session to a different destination address.</span></span> <span data-ttu-id="1c81d-105">L’interface TAPI permet à une application de spécifier une liste de conditions de transfert pour une adresse.</span><span class="sxs-lookup"><span data-stu-id="1c81d-105">TAPI allows an application to specify a list of forwarding conditions for an address.</span></span> <span data-ttu-id="1c81d-106">Les conditions de transfert peuvent être aussi finement grainées qu’une destination et un [**mode de transfert**](./lineforwardmode--constants.md) différents pour chaque adresse d’appelant.</span><span class="sxs-lookup"><span data-stu-id="1c81d-106">Forwarding conditions can be as finely grained as a different destination and [**forwarding mode**](./lineforwardmode--constants.md) for each caller address.</span></span>

<span data-ttu-id="1c81d-107">L’opération de transfert peut également être utilisée pour implémenter une fonctionnalité de do-not-sélective, en transférant certains appelants vers la messagerie vocale et en permettant à d’autres utilisateurs de tenter de se terminer.</span><span class="sxs-lookup"><span data-stu-id="1c81d-107">The forwarding operation can also be used to implement a selective do-not-disturb feature, by forwarding some callers to voice mail and allowing others to attempt completion.</span></span>

<span data-ttu-id="1c81d-108">L’opération de transfert peut également annuler tout transfert actuellement en vigueur.</span><span class="sxs-lookup"><span data-stu-id="1c81d-108">The forwarding operation can also cancel any forwarding currently in effect.</span></span>

<span data-ttu-id="1c81d-109">Certains fournisseurs de services requièrent qu’une application crée un appel de consultation avant une opération de transfert.</span><span class="sxs-lookup"><span data-stu-id="1c81d-109">Some service providers require that an application create a consultation call prior to a forwarding operation.</span></span> <span data-ttu-id="1c81d-110">Un pointeur désignant l’appel de consultation est ensuite passé à l’opération de transfert.</span><span class="sxs-lookup"><span data-stu-id="1c81d-110">The forwarding operation is then passed a pointer to the consultation call.</span></span>

<span data-ttu-id="1c81d-111">Les fournisseurs de services ne prennent pas tous en charge l’utilisation de cette opération.</span><span class="sxs-lookup"><span data-stu-id="1c81d-111">Not all service providers support use of this operation.</span></span>

<span data-ttu-id="1c81d-112">**TAPI 2. x :** Pour définir [**lineForward**](/windows/win32/api/tapi/nf-tapi-lineforward) sur [**lineGetAddressStatus**](/windows/win32/api/tapi/nf-tapi-linegetaddressstatus), modifiez la [**ligne \_ ADDRESSSTATE**](./line-addressstate.md) message de notification avec LINEADDRESSSTATE \_ Forward.</span><span class="sxs-lookup"><span data-stu-id="1c81d-112">**TAPI 2.x:** To set [**lineForward**](/windows/win32/api/tapi/nf-tapi-lineforward) to get [**lineGetAddressStatus**](/windows/win32/api/tapi/nf-tapi-linegetaddressstatus), change the [**LINE\_ADDRESSSTATE**](./line-addressstate.md) notification message with LINEADDRESSSTATE\_FORWARD.</span></span>

<span data-ttu-id="1c81d-113">**TAPI 3. x :** Consultez [**ITAddress :: Forward**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward), [**ITAddress :: obtenir \_ CurrentForwardInfo**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_currentforwardinfo), change notification : [**ITAddressEvent :: obtenir un \_ événement**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddressevent-get_event) avec AE \_ Forward.</span><span class="sxs-lookup"><span data-stu-id="1c81d-113">**TAPI 3.x:** See [**ITAddress::Forward**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward), [**ITAddress::get\_CurrentForwardInfo**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_currentforwardinfo), change notification: [**ITAddressEvent::get\_Event**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddressevent-get_event) with AE\_FORWARD.</span></span>

> [!Note]  
> <span data-ttu-id="1c81d-114">Il peut être impossible pour un fournisseur de services de savoir à tout moment quel transfert est en vigueur pour une adresse.</span><span class="sxs-lookup"><span data-stu-id="1c81d-114">It may be impossible for a service provider to know at all times what forwarding is in effect for an address.</span></span> <span data-ttu-id="1c81d-115">Le transfert peut être annulé ou modifié de manière à ne pas envoyer de notification au fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="1c81d-115">Forwarding can be canceled or changed in ways that do not result in notification to the service provider.</span></span>

 

 

 
