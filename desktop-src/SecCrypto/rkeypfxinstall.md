---
description: La fonction RKeyPFXInstall n’est pas prise en charge.
ms.assetid: 061e3d9d-fc92-4204-92f3-f3425afdbe27
title: RKeyPFXInstall, fonction (Rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RKeyPFXInstall
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 4908b7224a02f5a28b876b1ff67cbcec7d23df5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951193"
---
# <a name="rkeypfxinstall-function"></a><span data-ttu-id="64635-103">RKeyPFXInstall fonction)</span><span class="sxs-lookup"><span data-stu-id="64635-103">RKeyPFXInstall function</span></span>

<span data-ttu-id="64635-104">La fonction **RKeyPFXInstall** n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="64635-104">The **RKeyPFXInstall** function is not supported.</span></span>

<span data-ttu-id="64635-105">**Windows Server 2003 :** La fonction **RKeyPFXInstall** installe un certificat sur un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="64635-105">**Windows Server 2003:** The **RKeyPFXInstall** function installs a certificate on a remote computer.</span></span> <span data-ttu-id="64635-106">Notez que ce comportement a changé avec Windows Server 2003 avec Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="64635-106">Note that this behavior has changed with Windows Server 2003 with Service Pack 1 (SP1).</span></span>

## <a name="syntax"></a><span data-ttu-id="64635-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="64635-107">Syntax</span></span>


```C++
ULONG RKeyPFXInstall(
  _In_ KEYSVCC_HANDLE         hKeySvcCli,
  _In_ PKEYSVC_BLOB           pPFX,
  _In_ PKEYSVC_UNICODE_STRING pPassword,
  _In_ ULONG                  ulFlags
);
```



## <a name="parameters"></a><span data-ttu-id="64635-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="64635-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64635-109">*hKeySvcCli* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="64635-109">*hKeySvcCli* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64635-110">Handle [**de \_ handle KEYSVCC**](keysvcc-handle.md) précédemment ouvert par [**RKeyOpenKeyService**](rkeyopenkeyservice.md).</span><span class="sxs-lookup"><span data-stu-id="64635-110">A [**KEYSVCC\_HANDLE**](keysvcc-handle.md) handle previously opened by [**RKeyOpenKeyService**](rkeyopenkeyservice.md).</span></span> <span data-ttu-id="64635-111">Le descripteur représente l’ordinateur distant qui recevra le certificat.</span><span class="sxs-lookup"><span data-stu-id="64635-111">The handle represents the remote computer that will receive the certificate.</span></span> <span data-ttu-id="64635-112">Cette valeur ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="64635-112">This value cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="64635-113">*pPFX* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="64635-113">*pPFX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64635-114">Pointeur vers une structure [**d' \_ objet BLOB KEYSVC**](keysvc-blob.md) qui représente le certificat à installer.</span><span class="sxs-lookup"><span data-stu-id="64635-114">A pointer to a [**KEYSVC\_BLOB**](keysvc-blob.md) structure that represents the certificate to install.</span></span> <span data-ttu-id="64635-115">L’objet BLOB est au format [*PKCS \# 12*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="64635-115">The BLOB is in [*PKCS \#12*](../secgloss/p-gly.md) format.</span></span>

</dd> <dt>

<span data-ttu-id="64635-116">*pPassword* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="64635-116">*pPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64635-117">Pointeur vers une structure [**de \_ \_ chaîne Unicode KEYSVC**](keysvc-unicode-string.md) qui représente le mot de passe pour l’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="64635-117">A pointer to a [**KEYSVC\_UNICODE\_STRING**](keysvc-unicode-string.md) structure that represents the password for the BLOB.</span></span> <span data-ttu-id="64635-118">Lorsque vous avez fini d’utiliser le mot de passe, effacez le mot de passe de la mémoire en appelant la fonction [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="64635-118">When you have finished using the password, clear the password from memory by calling the [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) function.</span></span> <span data-ttu-id="64635-119">Pour plus d’informations sur la protection des mots de passe, consultez [gestion des mots de passe](../secbp/handling-passwords.md).</span><span class="sxs-lookup"><span data-stu-id="64635-119">For more information about protecting passwords, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> <dt>

<span data-ttu-id="64635-120">*ulFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="64635-120">*ulFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64635-121">Indicateurs qui spécifient les options d’installation du certificat.</span><span class="sxs-lookup"><span data-stu-id="64635-121">Flags that specify the certificate installation options.</span></span> <span data-ttu-id="64635-122">Ce paramètre peut avoir la valeur zéro ou une combinaison des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="64635-122">This parameter can be a zero or a combination of the following values.</span></span>



| <span data-ttu-id="64635-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="64635-123">Value</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="64635-124">Signification</span><span class="sxs-lookup"><span data-stu-id="64635-124">Meaning</span></span>                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="CRYPT_EXPORTABLE"></span><span id="crypt_exportable"></span><dl> <span data-ttu-id="64635-125"><dt>**Crypt \_ Exportable**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="64635-125"><dt>**CRYPT\_EXPORTABLE**</dt> <dt></dt></span></span> </dl>              | <span data-ttu-id="64635-126">Les clés importées sont marquées comme étant exportables.</span><span class="sxs-lookup"><span data-stu-id="64635-126">Imported keys are marked as exportable.</span></span><br/>                                           |
| <span id="CRYPT_MACHINE_KEYSET"></span><span id="crypt_machine_keyset"></span><dl> <span data-ttu-id="64635-127"><dt>**Crypt \_ \_jeu de clés**</dt> de l’ordinateur <dt></dt></span><span class="sxs-lookup"><span data-stu-id="64635-127"><dt>**CRYPT\_MACHINE\_KEYSET**</dt> <dt></dt></span></span> </dl> | <span data-ttu-id="64635-128">Les clés privées sont stockées sous l’ordinateur distant et non sous l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="64635-128">Private keys are stored under the remote computer and not under the current user.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64635-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="64635-129">Return value</span></span>

<span data-ttu-id="64635-130">Si la fonction réussit, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="64635-130">If the function is successful, the return value is S\_OK.</span></span>

<span data-ttu-id="64635-131">Si la fonction échoue, la valeur de retour est un **ULong** qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="64635-131">If the function fails, the return value is a **ULONG** that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="64635-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="64635-132">Requirements</span></span>



| <span data-ttu-id="64635-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="64635-133">Requirement</span></span> | <span data-ttu-id="64635-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="64635-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="64635-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="64635-135">Minimum supported client</span></span><br/> | <span data-ttu-id="64635-136">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="64635-136">None supported</span></span><br/>                                                             |
| <span data-ttu-id="64635-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="64635-137">Minimum supported server</span></span><br/> | <span data-ttu-id="64635-138">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="64635-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="64635-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="64635-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="64635-140"><dt>Rkeysvcc. h</dt></span><span class="sxs-lookup"><span data-stu-id="64635-140"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64635-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64635-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64635-142">**RKeyCloseKeyService**</span><span class="sxs-lookup"><span data-stu-id="64635-142">**RKeyCloseKeyService**</span></span>](rkeyclosekeyservice.md)
</dt> <dt>

[<span data-ttu-id="64635-143">**RKeyOpenKeyService**</span><span class="sxs-lookup"><span data-stu-id="64635-143">**RKeyOpenKeyService**</span></span>](rkeyopenkeyservice.md)
</dt> </dl>

 

 
