---
description: Événements d’extension MTP
ms.assetid: c04554cd-d68d-455e-afa3-29d4186dad65
title: Événements d’extension MTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10389df9105615befa9ba0f32824615977cc3cb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518940"
---
# <a name="mtp-extension-events"></a><span data-ttu-id="0278e-103">Événements d’extension MTP</span><span class="sxs-lookup"><span data-stu-id="0278e-103">MTP Extension Events</span></span>

<span data-ttu-id="0278e-104">Les événements signalent à une application que des modifications ont été apportées sur un appareil ou avec celui-ci.</span><span class="sxs-lookup"><span data-stu-id="0278e-104">Events notify an application that changes have occurred on, or with, a device.</span></span> <span data-ttu-id="0278e-105">Par exemple, une application peut s’inscrire pour recevoir notifications qu’un appareil a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="0278e-105">For example, an application can register to receive notfications that a device has been removed .</span></span>

## <a name="vendor-extended-event-codes"></a><span data-ttu-id="0278e-106">Fournisseurs-codes d’événements étendus</span><span class="sxs-lookup"><span data-stu-id="0278e-106">Vendor-Extended Event Codes</span></span>

<span data-ttu-id="0278e-107">Lorsqu’un fabricant d’appareils prend en charge un événement étendu par un fournisseur, son pilote combine le code d’événement du fournisseur (UINT16) et les 16 bits les plus élevés du GUID des **\_ \_ \_ \_ \_ événements étendus du fournisseur** d’événements MTP.</span><span class="sxs-lookup"><span data-stu-id="0278e-107">When a device manufacturer supports a vendor-extended event, their driver combines the vendor's event code (UINT16) with the highest 16 bits of the **WPD\_EVENT\_MTP\_VENDOR\_EXTENDED\_EVENTS** GUID.</span></span>

<span data-ttu-id="0278e-108">Par exemple, si le code étendu du fournisseur est 0xC001, le GUID résultant est comme indiqué dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="0278e-108">For example, if the vendor-extended code is 0xC001, the resulting GUID would be as shown in the following example:</span></span>


```C++
{C0010000-5738-4ff2-8445-BE3126691059}
```



## <a name="vendor-extended-event-parameters"></a><span data-ttu-id="0278e-109">Paramètres d’événement étendus du fournisseur</span><span class="sxs-lookup"><span data-stu-id="0278e-109">Vendor-Extended Event Parameters</span></span>

<span data-ttu-id="0278e-110">Les paramètres d’un événement étendu par le fournisseur sont signalés par le GUID d' **ID d’événement du \_ paramètre d’événement \_ \_ \_ wpd** et par la **propriété wpd paramètres d' \_ \_ \_ événement MTP ext \_ \_**, qui est une collection de **PROPVARIANTS**.</span><span class="sxs-lookup"><span data-stu-id="0278e-110">The parameters for a vendor-extended event are reported by the **WPD\_EVENT\_PARAMETER\_EVENT\_ID** GUID and the **WPD\_PROPERTY\_MTP\_EXT\_EVENT\_PARAMS**, which is a collection of **PROPVARIANTS**.</span></span> <span data-ttu-id="0278e-111">Ces **PROPVARIANTS** correspondent aux paramètres d’événement.</span><span class="sxs-lookup"><span data-stu-id="0278e-111">These **PROPVARIANTS** correspond to the event parameters.</span></span> <span data-ttu-id="0278e-112">S’il n’y a aucun paramètre, cette collection est vide.</span><span class="sxs-lookup"><span data-stu-id="0278e-112">If there are no parameters, this collection is empty.</span></span>


```C++
{C0010000-5738-4ff2-8445-BE3126691059}
```



## <a name="related-topics"></a><span data-ttu-id="0278e-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0278e-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0278e-114">Prise en charge des extensions MTP</span><span class="sxs-lookup"><span data-stu-id="0278e-114">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 



