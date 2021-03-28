---
description: Transfère les événements de l’objet ShellFolderView spécifié au gestionnaire d’événements ShellFolderViewOC correspondant.
ms.assetid: 44a2a0a5-aa87-43ae-b4ea-0d301fcb8464
title: Méthode ShellFolderViewOC. SetFolderView (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderViewOC.SetFolderView
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 7d331fadbd8abae62ee896caec772d84d079f88d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973583"
---
# <a name="shellfolderviewocsetfolderview-method"></a><span data-ttu-id="651a0-103">Méthode ShellFolderViewOC. SetFolderView</span><span class="sxs-lookup"><span data-stu-id="651a0-103">ShellFolderViewOC.SetFolderView method</span></span>

<span data-ttu-id="651a0-104">Transfère les événements de l’objet [**ShellFolderView**](shellfolderview.md) spécifié au gestionnaire d’événements [**ShellFolderViewOC**](shellfolderviewoc-object.md) correspondant.</span><span class="sxs-lookup"><span data-stu-id="651a0-104">Forwards the events of the specified [**ShellFolderView**](shellfolderview.md) object to the corresponding [**ShellFolderViewOC**](shellfolderviewoc-object.md) event handler.</span></span>

## <a name="syntax"></a><span data-ttu-id="651a0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="651a0-105">Syntax</span></span>


```JScript
iRetVal = ShellFolderViewOC.SetFolderView(
  oShellFolderView
)
```



## <a name="parameters"></a><span data-ttu-id="651a0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="651a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="651a0-107">*oShellFolderView* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="651a0-107">*oShellFolderView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="651a0-108">Type : \**[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) \** _</span><span class="sxs-lookup"><span data-stu-id="651a0-108">Type: \**[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\** _</span></span>

<span data-ttu-id="651a0-109">Objet [_ *ShellFolderView* \*](shellfolderview.md) .</span><span class="sxs-lookup"><span data-stu-id="651a0-109">A [_ *ShellFolderView*\*](shellfolderview.md) object.</span></span> <span data-ttu-id="651a0-110">Ses événements [**EnumDone**](shellfolderviewoc-enumdone.md) et [**SelectionChanged**](shellfolderview-selectionchanged.md) seront transmis au gestionnaire d’événements [**ShellFolderViewOC**](shellfolderviewoc-object.md) correspondant.</span><span class="sxs-lookup"><span data-stu-id="651a0-110">Its [**EnumDone**](shellfolderviewoc-enumdone.md) and [**SelectionChanged**](shellfolderview-selectionchanged.md) events will be forwarded to the corresponding [**ShellFolderViewOC**](shellfolderviewoc-object.md) event handler.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="651a0-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="651a0-111">Requirements</span></span>



| <span data-ttu-id="651a0-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="651a0-112">Requirement</span></span> | <span data-ttu-id="651a0-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="651a0-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="651a0-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="651a0-114">Minimum supported client</span></span><br/> | <span data-ttu-id="651a0-115">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="651a0-115">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="651a0-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="651a0-116">Minimum supported server</span></span><br/> | <span data-ttu-id="651a0-117">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="651a0-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="651a0-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="651a0-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="651a0-119"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="651a0-119"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="651a0-120">MIDL</span><span class="sxs-lookup"><span data-stu-id="651a0-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="651a0-121"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="651a0-121"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="651a0-122">DLL</span><span class="sxs-lookup"><span data-stu-id="651a0-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="651a0-123"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="651a0-123"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
