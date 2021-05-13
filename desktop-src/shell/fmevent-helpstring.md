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
ms.openlocfilehash: 6fe187330e27f7e246c9bbd68005f68f346bbc90
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841280"
---
# <a name="fmevent_helpstring-message"></a><span data-ttu-id="59c7e-103">\_Message FMEVENT HELPSTRING</span><span class="sxs-lookup"><span data-stu-id="59c7e-103">FMEVENT\_HELPSTRING message</span></span>

<span data-ttu-id="59c7e-104">Envoyé à une procédure DLL d’extension du gestionnaire de fichiers lorsque le gestionnaire de fichiers souhaite une chaîne d’aide pour un élément de commande de menu ou de barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="59c7e-104">Sent to a File Manager extension DLL procedure when File Manager wants a Help string for a menu or toolbar command item.</span></span>

## <a name="parameters"></a><span data-ttu-id="59c7e-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="59c7e-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59c7e-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="59c7e-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="59c7e-107">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="59c7e-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="59c7e-108">*lpfmshs*</span><span class="sxs-lookup"><span data-stu-id="59c7e-108">*lpfmshs*</span></span> 
</dt> <dd>

<span data-ttu-id="59c7e-109">Adresse d’une structure [**\_ HELPSTRING de FMS**](fms-helpstring.md) qui communique les données de chaîne d’aide de l’élément de commande.</span><span class="sxs-lookup"><span data-stu-id="59c7e-109">The address of an [**FMS\_HELPSTRING**](fms-helpstring.md) structure that communicates command item Help string data.</span></span> <span data-ttu-id="59c7e-110">La **structure \_ HELPSTRING de FMS** identifie l’élément de commande pour lequel une chaîne d’aide est souhaitée, ainsi qu’un handle vers son menu.</span><span class="sxs-lookup"><span data-stu-id="59c7e-110">The **FMS\_HELPSTRING** structure identifies the command item for which a Help string is wanted, along with a handle to its menu.</span></span> <span data-ttu-id="59c7e-111">Une application écrit ensuite la chaîne d’aide appropriée dans le membre **szHelp** de la structure **\_ HELPSTRING de FMS** .</span><span class="sxs-lookup"><span data-stu-id="59c7e-111">An application then writes the appropriate Help string to the **FMS\_HELPSTRING** structure's **szHelp** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59c7e-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="59c7e-112">Return value</span></span>

<span data-ttu-id="59c7e-113">Une procédure DLL d’extension doit retourner zéro si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="59c7e-113">An extension DLL procedure should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="59c7e-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="59c7e-114">Requirements</span></span>



| <span data-ttu-id="59c7e-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="59c7e-115">Requirement</span></span> | <span data-ttu-id="59c7e-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="59c7e-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="59c7e-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59c7e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="59c7e-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="59c7e-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="59c7e-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59c7e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="59c7e-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="59c7e-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="59c7e-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="59c7e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="59c7e-122"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="59c7e-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59c7e-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59c7e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59c7e-124">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="59c7e-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="59c7e-125">**FMEVENT \_ HELPMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="59c7e-125">**FMEVENT\_HELPMENUITEM**</span></span>](fmevent-helpmenuitem.md)
</dt> </dl>

 

 




