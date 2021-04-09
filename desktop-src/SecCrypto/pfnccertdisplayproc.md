---
description: Fonction de rappel définie par l’utilisateur qui permet à l’appelant de la fonction CryptUIDlgSelectCertificate de gérer l’affichage des certificats que l’utilisateur sélectionne pour afficher.
ms.assetid: fdb9e9e0-02f1-42e0-9a11-204d916a1a88
title: PFNCCERTDISPLAYPROC fonction de rappel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PFNCCERTDISPLAYPROC
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 7371e983b339ff8bfa9edb1b7fb795ab64596a98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034571"
---
# <a name="pfnccertdisplayproc-callback-function"></a><span data-ttu-id="45c4a-103">PFNCCERTDISPLAYPROC fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="45c4a-103">PFNCCERTDISPLAYPROC callback function</span></span>

<span data-ttu-id="45c4a-104">La fonction **PFNCCERTDISPLAYPROC** est une fonction de rappel définie par l’utilisateur qui permet à l’appelant de la fonction [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) de gérer l’affichage des certificats que l’utilisateur sélectionne pour afficher.</span><span class="sxs-lookup"><span data-stu-id="45c4a-104">The **PFNCCERTDISPLAYPROC** function is a user-defined callback function that allows the caller of the [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) function to handle the display of certificates that the user selects to view.</span></span>

## <a name="syntax"></a><span data-ttu-id="45c4a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="45c4a-105">Syntax</span></span>


```C++
BOOL WINAPI * PFNCCERTDISPLAYPROC(
  _In_ PCCERT_CONTEXT pCertContext,
  _In_ HWND           hWndSelCertDlg,
  _In_ void           *pvCallbackData
);
```



## <a name="parameters"></a><span data-ttu-id="45c4a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="45c4a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45c4a-107">*pCertContext* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="45c4a-107">*pCertContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45c4a-108">Pointeur vers une structure [**de \_ contexte de certificat**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) qui représente le certificat à afficher.</span><span class="sxs-lookup"><span data-stu-id="45c4a-108">A pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) structure that represents the certificate to display.</span></span>

</dd> <dt>

<span data-ttu-id="45c4a-109">*hWndSelCertDlg* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="45c4a-109">*hWndSelCertDlg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45c4a-110">Handle de la boîte de dialogue à partir de laquelle le certificat a été sélectionné pour être affiché.</span><span class="sxs-lookup"><span data-stu-id="45c4a-110">A handle to the dialog box from which the certificate was selected for viewing.</span></span>

</dd> <dt>

<span data-ttu-id="45c4a-111">*pvCallbackData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="45c4a-111">*pvCallbackData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45c4a-112">Données supplémentaires utilisées par la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="45c4a-112">Additional data used by the callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45c4a-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="45c4a-113">Return value</span></span>

<span data-ttu-id="45c4a-114">Cette fonction retourne **true** pour indiquer qu’elle gère l’affichage du certificat et que la boîte de dialogue ne doit pas afficher le certificat.</span><span class="sxs-lookup"><span data-stu-id="45c4a-114">This function returns **TRUE** to indicate that it handles display of the certificate and that the dialog box should not display the certificate.</span></span> <span data-ttu-id="45c4a-115">Si cette fonction retourne la **valeur false**, la boîte de dialogue affiche le certificat.</span><span class="sxs-lookup"><span data-stu-id="45c4a-115">If this function returns **FALSE**, the dialog box displays the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="45c4a-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="45c4a-116">Requirements</span></span>



| <span data-ttu-id="45c4a-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="45c4a-117">Requirement</span></span> | <span data-ttu-id="45c4a-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="45c4a-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="45c4a-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="45c4a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="45c4a-120">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="45c4a-120">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="45c4a-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="45c4a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="45c4a-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="45c4a-122">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 




