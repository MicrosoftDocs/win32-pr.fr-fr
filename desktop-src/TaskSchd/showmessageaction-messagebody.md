---
title: ShowMessageAction. MessageBody, propriété
description: Pour les scripts, obtient ou définit le texte du message qui s’affiche dans le corps de la boîte de message.
ms.assetid: 7166e379-95f0-43f1-93a0-6a3d706dd627
keywords:
- Planificateur de tâches de la propriété MessageBody
- Planificateur de tâches de la propriété MessageBody, objet ShowMessageAction
- Planificateur de tâches objet ShowMessageAction, propriété MessageBody
topic_type:
- apiref
api_name:
- ShowMessageAction.MessageBody
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1604367a8daad1ae1b5f44c6021d22bf1aa7c5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843261"
---
# <a name="showmessageactionmessagebody-property"></a><span data-ttu-id="30434-106">ShowMessageAction. MessageBody, propriété</span><span class="sxs-lookup"><span data-stu-id="30434-106">ShowMessageAction.MessageBody property</span></span>

<span data-ttu-id="30434-107">\[Cet objet n’est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="30434-107">\[This object is no longer supported.</span></span> <span data-ttu-id="30434-108">Vous pouvez utiliser IExecAction avec la fonction Windows Scripting [**MsgBox**](/previous-versions/sfw6660x(v=vs.80)) pour afficher un message dans la session utilisateur.\]</span><span class="sxs-lookup"><span data-stu-id="30434-108">You can use IExecAction with the Windows scripting [**MsgBox function**](/previous-versions/sfw6660x(v=vs.80)) to show a message in the user session.\]</span></span>

<span data-ttu-id="30434-109">Pour les scripts, obtient ou définit le texte du message qui s’affiche dans le corps de la boîte de message.</span><span class="sxs-lookup"><span data-stu-id="30434-109">For scripting, gets or sets the message text that is displayed in the body of the message box.</span></span>

## <a name="syntax"></a><span data-ttu-id="30434-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="30434-110">Syntax</span></span>


```VB
ShowMessageAction.MessageBody As String
```



## <a name="property-value"></a><span data-ttu-id="30434-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="30434-111">Property value</span></span>

<span data-ttu-id="30434-112">Texte du message affiché dans le corps de la boîte de message.</span><span class="sxs-lookup"><span data-stu-id="30434-112">The message text that is displayed in the body of the message box.</span></span>

## <a name="remarks"></a><span data-ttu-id="30434-113">Notes</span><span class="sxs-lookup"><span data-stu-id="30434-113">Remarks</span></span>

<span data-ttu-id="30434-114">Les chaînes paramétrables peuvent être utilisées dans le texte du message de la boîte de message.</span><span class="sxs-lookup"><span data-stu-id="30434-114">Parameterized strings can be used in the message text of the message box.</span></span> <span data-ttu-id="30434-115">Pour plus d’informations, consultez la section exemples dans [**EventTrigger. ValueQueries**](eventtrigger-valuequeries.md).</span><span class="sxs-lookup"><span data-stu-id="30434-115">For more information, see the Examples section in [**EventTrigger.ValueQueries**](eventtrigger-valuequeries.md).</span></span>

<span data-ttu-id="30434-116">Lors de la définition de cette valeur de propriété, la valeur peut être un texte récupéré à partir d’un fichier Resource. dll.</span><span class="sxs-lookup"><span data-stu-id="30434-116">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="30434-117">Une chaîne spécialisée est utilisée pour référencer le texte à partir du fichier de ressources.</span><span class="sxs-lookup"><span data-stu-id="30434-117">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="30434-118">Le format de la chaîne est $ (@ \[ dll \] , \[ ResourceId \] ), où \[ dll \] est le chemin d’accès au fichier. dll qui contient la ressource et \[ ResourceId \] est l’identificateur du texte de la ressource.</span><span class="sxs-lookup"><span data-stu-id="30434-118">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="30434-119">Par exemple, si vous affectez la valeur $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101) à cette propriété, vous affectez à la propriété la valeur du texte de la ressource avec un identificateur égal à-101 dans le fichier% systemroot% \\ system32 \\ResourceName.dll.</span><span class="sxs-lookup"><span data-stu-id="30434-119">For example, the setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="30434-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="30434-120">Requirements</span></span>



| <span data-ttu-id="30434-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30434-121">Requirement</span></span> | <span data-ttu-id="30434-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="30434-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="30434-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30434-123">Minimum supported client</span></span><br/> | <span data-ttu-id="30434-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="30434-124">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="30434-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30434-125">Minimum supported server</span></span><br/> | <span data-ttu-id="30434-126">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="30434-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="30434-127">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="30434-127">End of client support</span></span><br/>    | <span data-ttu-id="30434-128">Windows 7</span><span class="sxs-lookup"><span data-stu-id="30434-128">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="30434-129">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="30434-129">End of server support</span></span><br/>    | <span data-ttu-id="30434-130">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="30434-130">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="30434-131">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="30434-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="30434-132"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="30434-132"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="30434-133">DLL</span><span class="sxs-lookup"><span data-stu-id="30434-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30434-134"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30434-134"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30434-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30434-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30434-136">**ShowMessageAction**</span><span class="sxs-lookup"><span data-stu-id="30434-136">**ShowMessageAction**</span></span>](showmessageaction.md)
</dt> </dl>

 

