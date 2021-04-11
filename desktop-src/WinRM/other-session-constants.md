---
title: Autres constantes de session (WSManDisp. h)
description: Spécifiez l’encodage, le chiffrement et le port du nom de principal du service.
ms.assetid: a921b7bc-1f40-427c-971f-c0bc9c9f6887
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WSManFlagUTF8
- WSManFlagNoEncryption
- WSManFlagEnableSPNServerPort
- WSManFlagUTF16
api_location:
- WSManDisp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 236e69d80db2ad30b8cc2934b6b2016d7eecbed6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105631"
---
# <a name="other-session-constants"></a><span data-ttu-id="b165c-103">Autres constantes de session</span><span class="sxs-lookup"><span data-stu-id="b165c-103">Other Session Constants</span></span>

<span data-ttu-id="b165c-104">Les constantes, répertoriées dans la liste suivante, dans l’énumération **\_ \_ WSManSessionFlags** qui spécifient l’encodage, le chiffrement et le port du nom de principal du service.</span><span class="sxs-lookup"><span data-stu-id="b165c-104">Constants, listed in the following list, in the **\_\_WSManSessionFlags** enumeration that specify encoding, encryption, and service principal name port.</span></span>

<dl> <dt>

<span data-ttu-id="b165c-105"><span id="WSManFlagUTF8"></span><span id="wsmanflagutf8"></span><span id="WSMANFLAGUTF8"></span>**WSManFlagUTF8**</span><span class="sxs-lookup"><span data-stu-id="b165c-105"><span id="WSManFlagUTF8"></span><span id="wsmanflagutf8"></span><span id="WSMANFLAGUTF8"></span>**WSManFlagUTF8**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b165c-106">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="b165c-106">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="b165c-107">Envoie la demande en UTF8 plutôt qu’en UTF16.</span><span class="sxs-lookup"><span data-stu-id="b165c-107">Sends the request in UTF8 rather than UTF16.</span></span>

<span data-ttu-id="b165c-108">La méthode de script associée est [**WSMan. SessionFlagUTF8**](wsman-sessionflagutf8.md) et la méthode C++ est [**IWSManEx. SessionFlagUTF8**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagutf8).</span><span class="sxs-lookup"><span data-stu-id="b165c-108">The associated scripting method is [**WSMan.SessionFlagUTF8**](wsman-sessionflagutf8.md) and the C++ method is [**IWSManEx.SessionFlagUTF8**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagutf8).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b165c-109"><span id="WSManFlagNoEncryption"></span><span id="wsmanflagnoencryption"></span><span id="WSMANFLAGNOENCRYPTION"></span>**WSManFlagNoEncryption**</span><span class="sxs-lookup"><span data-stu-id="b165c-109"><span id="WSManFlagNoEncryption"></span><span id="wsmanflagnoencryption"></span><span id="WSMANFLAGNOENCRYPTION"></span>**WSManFlagNoEncryption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b165c-110">1048576 ()</span><span class="sxs-lookup"><span data-stu-id="b165c-110">1048576 (0x100000)</span></span>
</dt> <dt>



<span data-ttu-id="b165c-111">Ne chiffrez pas les messages envoyés sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="b165c-111">Do not encrypt the messages sent over the network.</span></span> <span data-ttu-id="b165c-112">Ce paramètre est autorisé uniquement si l' [*écouteur*](windows-remote-management-glossary.md) est configuré de sorte que **AllowUnencrypted** ait la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="b165c-112">This setting is allowed only if the [*listener*](windows-remote-management-glossary.md) is configured so that **AllowUnencrypted** is set to **True**.</span></span>

<span data-ttu-id="b165c-113">La méthode de script associée est [**WSMan. SessionFlagNoEncryption**](wsman-sessionflagnoencryption.md) et la méthode C++ est [**IWSManEx. SessionFlagNoEncryption**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption).</span><span class="sxs-lookup"><span data-stu-id="b165c-113">The associated scripting method is [**WSMan.SessionFlagNoEncryption**](wsman-sessionflagnoencryption.md) and the C++ method is [**IWSManEx.SessionFlagNoEncryption**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b165c-114"><span id="WSManFlagEnableSPNServerPort"></span><span id="wsmanflagenablespnserverport"></span><span id="WSMANFLAGENABLESPNSERVERPORT"></span>**WSManFlagEnableSPNServerPort**</span><span class="sxs-lookup"><span data-stu-id="b165c-114"><span id="WSManFlagEnableSPNServerPort"></span><span id="wsmanflagenablespnserverport"></span><span id="WSMANFLAGENABLESPNSERVERPORT"></span>**WSManFlagEnableSPNServerPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b165c-115">4194304 (0x400000)</span><span class="sxs-lookup"><span data-stu-id="b165c-115">4194304 (0x400000)</span></span>
</dt> <dt>



<span data-ttu-id="b165c-116">Spécifiez le port du nom de principal du service (SPN) lors de la connexion directe au matériel BMC distant, également appelé connexion [*hors bande*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="b165c-116">Specify the Service Principal Name (SPN) port when connecting directly to remote BMC hardware, also known as an [*out-of-band*](windows-remote-management-glossary.md) connection.</span></span> <span data-ttu-id="b165c-117">Étant donné que l’ordinateur serveur WinRM et le matériel BMC peuvent partager la même adresse IP, cet indicateur indique que le numéro de port SPN doit être utilisé pour déterminer si la connexion concerne le service ou directement au contrôleur BMC.</span><span class="sxs-lookup"><span data-stu-id="b165c-117">Because both the WinRM server computer and the BMC hardware can share the same IP address, this flag indicates that the SPN port number must be used to determine whether the connection is to the service or directly to the BMC.</span></span> <span data-ttu-id="b165c-118">Pour plus d’informations, consultez [formats de noms pour les noms de principal du service uniques](/windows/desktop/AD/name-formats-for-unique-spns).</span><span class="sxs-lookup"><span data-stu-id="b165c-118">For more information, see [Name Formats for Unique SPNs](/windows/desktop/AD/name-formats-for-unique-spns).</span></span>

<span data-ttu-id="b165c-119">La méthode de script associée est [**WSMan. SessionFlagEnableSPNServerPort**](wsman-sessionflagenablespnserverport.md) et la méthode C++ est [**IWSManEx. SessionFlagEnableSPNServerPort**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagenablespnserverport).</span><span class="sxs-lookup"><span data-stu-id="b165c-119">The associated scripting method is [**WSMan.SessionFlagEnableSPNServerPort**](wsman-sessionflagenablespnserverport.md) and the C++ method is [**IWSManEx.SessionFlagEnableSPNServerPort**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagenablespnserverport).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b165c-120"><span id="WSManFlagUTF16"></span><span id="wsmanflagutf16"></span><span id="WSMANFLAGUTF16"></span>**WSManFlagUTF16**</span><span class="sxs-lookup"><span data-stu-id="b165c-120"><span id="WSManFlagUTF16"></span><span id="wsmanflagutf16"></span><span id="WSMANFLAGUTF16"></span>**WSManFlagUTF16**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b165c-121">0x800000</span><span class="sxs-lookup"><span data-stu-id="b165c-121">0x800000</span></span>
</dt> <dt>



<span data-ttu-id="b165c-122">Envoie la requête dans UTF16.</span><span class="sxs-lookup"><span data-stu-id="b165c-122">Sends the request in UTF16.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b165c-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b165c-123">Requirements</span></span>



| <span data-ttu-id="b165c-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b165c-124">Requirement</span></span> | <span data-ttu-id="b165c-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="b165c-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b165c-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b165c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b165c-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b165c-127">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="b165c-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b165c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b165c-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b165c-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="b165c-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="b165c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="b165c-131"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b165c-131"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b165c-132">MIDL</span><span class="sxs-lookup"><span data-stu-id="b165c-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b165c-133"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b165c-133"><dt>WSManDisp.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b165c-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b165c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b165c-135">Constantes de session</span><span class="sxs-lookup"><span data-stu-id="b165c-135">Session Constants</span></span>](session-constants.md)
</dt> </dl>

 

