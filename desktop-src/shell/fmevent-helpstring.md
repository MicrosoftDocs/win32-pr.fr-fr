---
description: Envoyé à une procédure DLL d’extension du gestionnaire de fichiers lorsque le gestionnaire de fichiers souhaite une chaîne d’aide pour un élément de commande de menu ou de barre d’outils.
title: Message FMEVENT_HELPSTRING (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_HELPSTRING
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 55fb5bfe-2889-40e5-9798-85f63727e31f
ms.openlocfilehash: ae3be1953d4c8bbf70f8f17fcf34fcfb1ac583f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202793"
---
# <a name="fmevent_helpstring-message"></a><span data-ttu-id="b9388-103">\_Message FMEVENT HELPSTRING</span><span class="sxs-lookup"><span data-stu-id="b9388-103">FMEVENT\_HELPSTRING message</span></span>

<span data-ttu-id="b9388-104">Envoyé à une procédure DLL d’extension du gestionnaire de fichiers lorsque le gestionnaire de fichiers souhaite une chaîne d’aide pour un élément de commande de menu ou de barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="b9388-104">Sent to a File Manager extension DLL procedure when File Manager wants a Help string for a menu or toolbar command item.</span></span>

## <a name="parameters"></a><span data-ttu-id="b9388-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b9388-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9388-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b9388-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b9388-107">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="b9388-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b9388-108">*lpfmshs*</span><span class="sxs-lookup"><span data-stu-id="b9388-108">*lpfmshs*</span></span> 
</dt> <dd>

<span data-ttu-id="b9388-109">Adresse d’une structure [**\_ HELPSTRING de FMS**](fms-helpstring.md) qui communique les données de chaîne d’aide de l’élément de commande.</span><span class="sxs-lookup"><span data-stu-id="b9388-109">The address of an [**FMS\_HELPSTRING**](fms-helpstring.md) structure that communicates command item Help string data.</span></span> <span data-ttu-id="b9388-110">La **structure \_ HELPSTRING de FMS** identifie l’élément de commande pour lequel une chaîne d’aide est souhaitée, ainsi qu’un handle vers son menu.</span><span class="sxs-lookup"><span data-stu-id="b9388-110">The **FMS\_HELPSTRING** structure identifies the command item for which a Help string is wanted, along with a handle to its menu.</span></span> <span data-ttu-id="b9388-111">Une application écrit ensuite la chaîne d’aide appropriée dans le membre **szHelp** de la structure **\_ HELPSTRING de FMS** .</span><span class="sxs-lookup"><span data-stu-id="b9388-111">An application then writes the appropriate Help string to the **FMS\_HELPSTRING** structure's **szHelp** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9388-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b9388-112">Return value</span></span>

<span data-ttu-id="b9388-113">Une procédure DLL d’extension doit retourner zéro si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="b9388-113">An extension DLL procedure should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9388-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b9388-114">Requirements</span></span>



| <span data-ttu-id="b9388-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b9388-115">Requirement</span></span> | <span data-ttu-id="b9388-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="b9388-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b9388-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b9388-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b9388-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b9388-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="b9388-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b9388-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b9388-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b9388-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b9388-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="b9388-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9388-122"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9388-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9388-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9388-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9388-124">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="b9388-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="b9388-125">**FMEVENT \_ HELPMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="b9388-125">**FMEVENT\_HELPMENUITEM**</span></span>](fmevent-helpmenuitem.md)
</dt> </dl>

 

 




