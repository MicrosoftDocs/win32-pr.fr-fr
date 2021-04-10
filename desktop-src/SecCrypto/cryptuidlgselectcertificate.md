---
description: Affiche une boîte de dialogue qui permet à un utilisateur de sélectionner un certificat.
ms.assetid: 242c19a7-179b-4fc0-a050-a1b598566a6b
title: CryptUIDlgSelectCertificate, fonction
ms.topic: reference
ms.date: 05/29/2020
ms.openlocfilehash: 65d9993cd1e035473e731056d33b7a391ef47b5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210435"
---
# <a name="cryptuidlgselectcertificate-function"></a><span data-ttu-id="a64e2-103">CryptUIDlgSelectCertificate, fonction</span><span class="sxs-lookup"><span data-stu-id="a64e2-103">CryptUIDlgSelectCertificate function</span></span>

<span data-ttu-id="a64e2-104">La fonction **CryptUIDlgSelectCertificate** affiche une boîte de dialogue qui permet à un utilisateur de sélectionner un certificat.</span><span class="sxs-lookup"><span data-stu-id="a64e2-104">The **CryptUIDlgSelectCertificate** function displays a dialog box that allows a user to select a certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="a64e2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a64e2-105">Syntax</span></span>


```C++
);
```



## <a name="parameters"></a><span data-ttu-id="a64e2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a64e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a64e2-107">*PCSC* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a64e2-107">*pcsc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a64e2-108">Pointeur vers une structure [**de \_ \_ struct SELECTCERTIFICATE**](cryptui-selectcertificate-struct.md) qui contient des informations sur la boîte de dialogue à afficher.</span><span class="sxs-lookup"><span data-stu-id="a64e2-108">A pointer to a [**CRYPTUI\_SELECTCERTIFICATE\_STRUCT**](cryptui-selectcertificate-struct.md) structure that contains information about the dialog box to display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a64e2-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a64e2-109">Return value</span></span>

<span data-ttu-id="a64e2-110">Pointeur vers une structure [**de \_ contexte de certificat**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) qui représente le certificat sélectionné par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a64e2-110">A pointer to a [**CERT\_CONTEXT**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) structure that represents the certificate selected by the user.</span></span> <span data-ttu-id="a64e2-111">Lorsque vous avez fini d’utiliser ce certificat, vous devez passer ce pointeur à la fonction [**CertFreeCertificateContext**](/windows/win32/api/wincrypt/nf-wincrypt-certfreecertificatecontext) pour décrémenter le décompte de références du contexte de certificat.</span><span class="sxs-lookup"><span data-stu-id="a64e2-111">When you have finished using this certificate, you must pass this pointer to the [**CertFreeCertificateContext**](/windows/win32/api/wincrypt/nf-wincrypt-certfreecertificatecontext) function to decrement the reference count of the certificate context.</span></span>

<span data-ttu-id="a64e2-112">Si le membre **dwFlags** de la structure *PCSC* ne contient pas l’indicateur de **\_ \_ multisélection CRYPTUI SELECTCERT** , une valeur de retour **null** signifie que l’utilisateur a fermé la boîte de dialogue sans sélectionner de certificat.</span><span class="sxs-lookup"><span data-stu-id="a64e2-112">If the **dwFlags** member of the *pcsc* structure does not contain the **CRYPTUI\_SELECTCERT\_MULTISELECT** flag, a return value of **NULL** means that the user closed the dialog box without selecting a certificate.</span></span>

<span data-ttu-id="a64e2-113">Si le membre **dwFlags** de la structure *PCSC* contient l’indicateur **de \_ \_ multisélection CRYPTUI SELECTCERT** , cette fonction retourne toujours la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="a64e2-113">If the **dwFlags** member of the *pcsc* structure does contain the **CRYPTUI\_SELECTCERT\_MULTISELECT** flag, this function always returns **NULL**.</span></span> <span data-ttu-id="a64e2-114">Les certificats sélectionnés seront contenus dans le magasin de certificats représenté par le membre **hSelectedCertStore** de *PCSC*.</span><span class="sxs-lookup"><span data-stu-id="a64e2-114">The selected certificates will be contained in the certificate store that is represented by the **hSelectedCertStore** member of *pcsc*.</span></span> <span data-ttu-id="a64e2-115">Si le nombre de certificats dans le magasin est identique avant et après l’appel de **CryptUIDlgSelectCertificate**, l’utilisateur a fermé la boîte de dialogue sans sélectionner de certificats.</span><span class="sxs-lookup"><span data-stu-id="a64e2-115">If the number of certificates in the store is the same before and after calling **CryptUIDlgSelectCertificate**, the user closed the dialog box without selecting any certificates.</span></span>

## <a name="remarks"></a><span data-ttu-id="a64e2-116">Notes</span><span class="sxs-lookup"><span data-stu-id="a64e2-116">Remarks</span></span>

<span data-ttu-id="a64e2-117">Si le membre **dwFlags** de la structure du [**\_ \_ struct cryptui SELECTCERTIFICATE**](cryptui-selectcertificate-struct.md) a la **valeur \_ CRYPTUI SELECTCERT \_ Legacy**, la boîte de dialogue héritée s’affiche.</span><span class="sxs-lookup"><span data-stu-id="a64e2-117">If the **dwFlags** member of the [**CRYPTUI\_SELECTCERTIFICATE\_STRUCT**](cryptui-selectcertificate-struct.md) structure is set to **CRYPTUI\_SELECTCERT\_LEGACY**, the legacy dialog is displayed.</span></span> <span data-ttu-id="a64e2-118">Dans le cas contraire, la boîte de dialogue de sélection de certificat active s’affiche.</span><span class="sxs-lookup"><span data-stu-id="a64e2-118">Otherwise, the current certificate selection dialog is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="a64e2-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a64e2-119">Requirements</span></span>



| <span data-ttu-id="a64e2-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a64e2-120">Requirement</span></span> | <span data-ttu-id="a64e2-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="a64e2-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a64e2-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a64e2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a64e2-123">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a64e2-123">Windows�XP \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="a64e2-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a64e2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a64e2-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a64e2-125">Windows Server�2003 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="a64e2-126">Fin de la prise en charge</span><span class="sxs-lookup"><span data-stu-id="a64e2-126">End of support</span></span><br/> | <span data-ttu-id="a64e2-127">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a64e2-127">Windows�7 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="a64e2-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a64e2-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="a64e2-129"><dt>Cryptui. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a64e2-129"><dt>Cryptui.lib</dt></span></span> </dl>            |
| <span data-ttu-id="a64e2-130">DLL</span><span class="sxs-lookup"><span data-stu-id="a64e2-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a64e2-131"><dt>Cryptui.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a64e2-131"><dt>Cryptui.dll</dt></span></span> </dl>            |
| <span data-ttu-id="a64e2-132">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="a64e2-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a64e2-133">**CryptUIDlgSelectCertificateW** (Unicode) et **CryptUIDlgSelectCertificateA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a64e2-133">**CryptUIDlgSelectCertificateW** (Unicode) and **CryptUIDlgSelectCertificateA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a64e2-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a64e2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a64e2-135">**\_SELECTCERTIFICATE, \_ struct**</span><span class="sxs-lookup"><span data-stu-id="a64e2-135">**CRYPTUI\_SELECTCERTIFICATE\_STRUCT**</span></span>](cryptui-selectcertificate-struct.md)
</dt> </dl>

<span data-ttu-id="a64e2-136">�</span><span class="sxs-lookup"><span data-stu-id="a64e2-136">�</span></span>

<span data-ttu-id="a64e2-137">�</span><span class="sxs-lookup"><span data-stu-id="a64e2-137">�</span></span>




