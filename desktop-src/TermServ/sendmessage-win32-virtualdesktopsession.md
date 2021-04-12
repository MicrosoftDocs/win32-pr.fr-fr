---
title: Méthode SendMessage de la classe Win32_VirtualDesktopSession
description: Envoyer un message à l’utilisateur via la session de bureau virtuel.
ms.assetid: 4bb9183e-c016-48f2-8e8c-0d5fb395c435
ms.tgt_platform: multiple
keywords:
- SendMessage, méthode Services Bureau à distance
- SendMessage, méthode Services Bureau à distance, classe Win32_VirtualDesktopSession
- Win32_VirtualDesktopSession de la classe Services Bureau à distance, SendMessage, méthode
topic_type:
- apiref
api_name:
- Win32_VirtualDesktopSession.SendMessage
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1e3e72f5c401b8cbb0e5e5de45f594d61af6275
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384572"
---
# <a name="sendmessage-method-of-the-win32_virtualdesktopsession-class"></a><span data-ttu-id="fdd34-106">Méthode SendMessage de la \_ classe VirtualDesktopSession Win32</span><span class="sxs-lookup"><span data-stu-id="fdd34-106">SendMessage method of the Win32\_VirtualDesktopSession class</span></span>

<span data-ttu-id="fdd34-107">Envoyer un message à l’utilisateur via la session de bureau virtuel.</span><span class="sxs-lookup"><span data-stu-id="fdd34-107">Send a message to the user through the virtual desktop session.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdd34-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fdd34-108">Syntax</span></span>


```mof
uint32 SendMessage(
  [in] string Title,
  [in] string Message
);
```



## <a name="parameters"></a><span data-ttu-id="fdd34-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fdd34-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdd34-110">*Titre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fdd34-110">*Title* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdd34-111">Titre du messages.</span><span class="sxs-lookup"><span data-stu-id="fdd34-111">The title of the messge.</span></span>

</dd> <dt>

<span data-ttu-id="fdd34-112">*Message* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fdd34-112">*Message* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdd34-113">Contenu du message.</span><span class="sxs-lookup"><span data-stu-id="fdd34-113">The content of the message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdd34-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fdd34-114">Return value</span></span>

<span data-ttu-id="fdd34-115">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="fdd34-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdd34-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fdd34-116">Requirements</span></span>



| <span data-ttu-id="fdd34-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fdd34-117">Requirement</span></span> | <span data-ttu-id="fdd34-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="fdd34-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdd34-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fdd34-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fdd34-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="fdd34-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="fdd34-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fdd34-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fdd34-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fdd34-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="fdd34-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fdd34-123">Namespace</span></span><br/>                | <span data-ttu-id="fdd34-124">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="fdd34-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="fdd34-125">MOF</span><span class="sxs-lookup"><span data-stu-id="fdd34-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fdd34-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fdd34-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="fdd34-127">DLL</span><span class="sxs-lookup"><span data-stu-id="fdd34-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fdd34-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fdd34-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="fdd34-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fdd34-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdd34-130">**\_VirtualDesktopSession Win32**</span><span class="sxs-lookup"><span data-stu-id="fdd34-130">**Win32\_VirtualDesktopSession**</span></span>](win32-virtualdesktopsession.md)
</dt> </dl>

 

 





