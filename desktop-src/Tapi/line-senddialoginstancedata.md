---
description: Le message SENDDIALOGINSTANCEDATA de la ligne TSPI fait que l’interface \_ TAPI appelle la \_ fonction TUISPI providerGenericDialogData dans la dll de l’interface utilisateur associée à htDlgInst, en lui transmettant le bloc de paramètres vers lequel pointe lpParams, de longueur dwSize nul.
ms.assetid: d3c176ba-8b4b-4b7c-a603-130dfa761898
title: Message LINE_SENDDIALOGINSTANCEDATA (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0af7ae5bfc942d4408ac5ce2438cd9a88c1f1f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540071"
---
# <a name="line_senddialoginstancedata-message"></a><span data-ttu-id="c61bc-103">\_Message SENDDIALOGINSTANCEDATA de ligne</span><span class="sxs-lookup"><span data-stu-id="c61bc-103">LINE\_SENDDIALOGINSTANCEDATA message</span></span>

<span data-ttu-id="c61bc-104">Le message **\_ SENDDIALOGINSTANCEDATA** de la ligne TSPI fait que l’interface TAPI appelle la fonction [**TUISPI \_ providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) dans la dll de l’interface utilisateur associée à *htDlgInst*, en lui transmettant le bloc de paramètres vers lequel pointe *lpParams, de* longueur *dwSize nul*.</span><span class="sxs-lookup"><span data-stu-id="c61bc-104">The TSPI **LINE\_SENDDIALOGINSTANCEDATA** message causes TAPI to call the [**TUISPI\_providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) function in the UI DLL associated with *htDlgInst*, passing it the parameter block pointed to by *lpParams*, of length *dwSize*.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="c61bc-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c61bc-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c61bc-106">*htDlgInst*</span><span class="sxs-lookup"><span data-stu-id="c61bc-106">*htDlgInst*</span></span> 
</dt> <dd>

<span data-ttu-id="c61bc-107">HTAPIDIALOGINSTANCE retourné au fournisseur de services lorsque l’instance de la boîte de dialogue a été créée à l’aide de la [**ligne \_ CREATEDIALOGINSTANCE**](line-createdialoginstance.md).</span><span class="sxs-lookup"><span data-stu-id="c61bc-107">The HTAPIDIALOGINSTANCE that was returned to the service provider when the dialog box instance was created using [**LINE\_CREATEDIALOGINSTANCE**](line-createdialoginstance.md).</span></span>

</dd> <dt>

<span data-ttu-id="c61bc-108">*lpParams*</span><span class="sxs-lookup"><span data-stu-id="c61bc-108">*lpParams*</span></span> 
</dt> <dd>

<span data-ttu-id="c61bc-109">Pointeur vers un bloc de paramètres spécifique au fournisseur qui est transmis à la fonction [**TUISPI \_ providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) de la dll de l’interface utilisateur, dont la taille est spécifiée par *dwSize nul*.</span><span class="sxs-lookup"><span data-stu-id="c61bc-109">Pointer to a provider-specific parameter block that is conveyed to the UI DLL [**TUISPI\_providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) function, the size of which is specified by *dwSize*.</span></span> <span data-ttu-id="c61bc-110">Si ce paramètre a la valeur **null**, il s’agit d’une demande de fermeture immédiate et de nettoyage de la boîte de dialogue (la dll de l’interface utilisateur ne doit pas appeler [**TUISPIDLLCALLBACK**](/windows/win32/api/tspi/nc-tspi-tuispidllcallback) pendant ce nettoyage).</span><span class="sxs-lookup"><span data-stu-id="c61bc-110">If this parameter is set to **NULL**, this is a request to close the dialog box immediately and clean up (the UI DLL should not invoke [**TUISPIDLLCALLBACK**](/windows/win32/api/tspi/nc-tspi-tuispidllcallback) during this cleanup).</span></span>

</dd> <dt>

<span data-ttu-id="c61bc-111">*dwSize nul*</span><span class="sxs-lookup"><span data-stu-id="c61bc-111">*dwSize*</span></span> 
</dt> <dd>

<span data-ttu-id="c61bc-112">Taille en octets du bloc de paramètres à transmettre à la DLL de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c61bc-112">The size in bytes of the parameter block to be conveyed to the UI DLL.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c61bc-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c61bc-113">Requirements</span></span>



| <span data-ttu-id="c61bc-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c61bc-114">Requirement</span></span> | <span data-ttu-id="c61bc-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="c61bc-115">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="c61bc-116">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="c61bc-116">TAPI version</span></span><br/> | <span data-ttu-id="c61bc-117">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="c61bc-117">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="c61bc-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="c61bc-118">Header</span></span><br/>       | <dl> <span data-ttu-id="c61bc-119"><dt>TSPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="c61bc-119"><dt>Tspi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c61bc-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c61bc-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c61bc-121">**TUISPIDLLCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="c61bc-121">**TUISPIDLLCALLBACK**</span></span>](/windows/win32/api/tspi/nc-tspi-tuispidllcallback)
</dt> <dt>

[<span data-ttu-id="c61bc-122">**TUISPI \_ providerGenericDialogData**</span><span class="sxs-lookup"><span data-stu-id="c61bc-122">**TUISPI\_providerGenericDialogData**</span></span>](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata)
</dt> <dt>

[<span data-ttu-id="c61bc-123">**CREATEDIALOGINSTANCE de ligne \_**</span><span class="sxs-lookup"><span data-stu-id="c61bc-123">**LINE\_CREATEDIALOGINSTANCE**</span></span>](line-createdialoginstance.md)
</dt> </dl>

 

