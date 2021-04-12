---
title: IAgentCharacter afficher
description: IAgentCharacter afficher
ms.assetid: 5f13dcef-3777-41eb-827f-6162bad71a2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 997a9879d564644085bd92e4515460c3dde33208
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031243"
---
# <a name="iagentcharactershow"></a><span data-ttu-id="5124a-103">IAgentCharacter :: Show</span><span class="sxs-lookup"><span data-stu-id="5124a-103">IAgentCharacter::Show</span></span>

<span data-ttu-id="5124a-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5124a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Show(
   long bFast,      // play Showing state animation flag
   long * pdwReqID  // address of request ID
);
```

<span data-ttu-id="5124a-105">Affiche un caractère.</span><span class="sxs-lookup"><span data-stu-id="5124a-105">Displays a character.</span></span>

-   <span data-ttu-id="5124a-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="5124a-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="5124a-107">Lorsque la fonction retourne, *pdwReqID* contient l’ID de la demande.</span><span class="sxs-lookup"><span data-stu-id="5124a-107">When the function returns, *pdwReqID* contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="5124a-108"><span id="bFast"></span><span id="bfast"></span><span id="BFAST"></span>*bFast*</span><span class="sxs-lookup"><span data-stu-id="5124a-108"><span id="bFast"></span><span id="bfast"></span><span id="BFAST"></span>*bFast*</span></span>
</dt> <dd>

<span data-ttu-id="5124a-109">Indication de l’indicateur d’animation d’État.</span><span class="sxs-lookup"><span data-stu-id="5124a-109">Showing state animation flag.</span></span> <span data-ttu-id="5124a-110">Si ce paramètre a la **valeur true**, l’animation de l’état d' **affichage** est lue après que le caractère a été visible ; Si la **valeur est false**, l’animation n’est pas lue.</span><span class="sxs-lookup"><span data-stu-id="5124a-110">If this parameter is **True**, the **Showing** state animation plays after making the character visible; if **False**, the animation does not play.</span></span>

</dd> <dt>

<span data-ttu-id="5124a-111"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="5124a-111"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="5124a-112">Adresse d’une variable qui reçoit l’ID de demande [**Show**](/windows/desktop/lwef/iagentcharacter--show) .</span><span class="sxs-lookup"><span data-stu-id="5124a-112">Address of a variable that receives the [**Show**](/windows/desktop/lwef/iagentcharacter--show) request ID.</span></span>

</dd> </dl>

<span data-ttu-id="5124a-113">Évitez d’affecter la **valeur true** au paramètre *bFast* sans avoir à utiliser une animation au préalable ; sinon, le frame de caractères peut être affiché, mais n’a aucune image à afficher.</span><span class="sxs-lookup"><span data-stu-id="5124a-113">Avoid setting the *bFast* parameter to **True** without playing an animation beforehand, otherwise, the character frame may be displayed, but have no image to display.</span></span> <span data-ttu-id="5124a-114">En particulier, Notez que si vous appelez [**MoveTo**](iagentcharacter--moveto.md) alors que le caractère n’est pas visible, aucune animation n’est lue.</span><span class="sxs-lookup"><span data-stu-id="5124a-114">In particular, note that if you call [**MoveTo**](iagentcharacter--moveto.md) when the character is not visible, it does not play any animation.</span></span> <span data-ttu-id="5124a-115">Par conséquent, si vous appelez la méthode **Show** avec *BFast* défini sur **true**, aucune image ne sera affichée.</span><span class="sxs-lookup"><span data-stu-id="5124a-115">Therefore, if you call the **Show** method with *bFast* set to **True**, no image will be displayed.</span></span> <span data-ttu-id="5124a-116">De même, si vous appelez [**Hide**](/windows/desktop/lwef/iagentcharacter--hide)et **Show** avec *bFast* défini sur **true**, il n’y aura aucune image visible.</span><span class="sxs-lookup"><span data-stu-id="5124a-116">Similarly, if you call [**Hide**](/windows/desktop/lwef/iagentcharacter--hide), then **Show** with *bFast* set to **True**, there will be no visible image.</span></span>

<span data-ttu-id="5124a-117">Lorsque vous utilisez le protocole HTTP pour accéder aux données de caractères et d’animation, utilisez la méthode [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) pour garantir la disponibilité de l’animation de l’état d' **émission** avant d’appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="5124a-117">When using the HTTP protocol to access character and animation data, use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to ensure the availability of the **Showing** state animation before calling this method.</span></span>

## <a name="see-also"></a><span data-ttu-id="5124a-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5124a-118">See Also</span></span>

[<span data-ttu-id="5124a-119">**IAgentCharacter :: Hide**</span><span class="sxs-lookup"><span data-stu-id="5124a-119">**IAgentCharacter::Hide**</span></span>](iagentcharacter--hide.md)


 

 