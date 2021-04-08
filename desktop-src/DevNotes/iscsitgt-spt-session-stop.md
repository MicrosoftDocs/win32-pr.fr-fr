---
description: Utilisé avec l' \_ IOCTL SCSI \_ miniport IOCTL et le \_ \_ \_ \_ Code de contrôle 0x101 (CTLCODE ISCSITGT SPT session end) pour arrêter une session.
ms.assetid: 74DAA560-A5BA-475C-AA36-7E6F0EA82EFE
title: Structure ISCSITGT_SPT_SESSION_STOP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCSITGT_SPT_SESSION_STOP
api_type:
- NA
api_location: ''
ms.openlocfilehash: e4501fbe2d1bbf884448d6b6a9476ee4782d3da7
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "103869673"
---
# <a name="iscsitgt_spt_session_stop-structure"></a><span data-ttu-id="9f1b5-103">\_Structure d' \_ arrêt de session SPT ISCSITGT \_</span><span class="sxs-lookup"><span data-stu-id="9f1b5-103">ISCSITGT\_SPT\_SESSION\_STOP structure</span></span>

<span data-ttu-id="9f1b5-104">\[La structure suivante peut être utilisée dans Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="9f1b5-104">\[The following structure is available for use in Windows Server 2012 R2.</span></span> <span data-ttu-id="9f1b5-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.\]</span><span class="sxs-lookup"><span data-stu-id="9f1b5-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="9f1b5-106">Utilisé avec l' [**IOCTL \_ SCSI \_ miniport**](/windows-hardware/drivers/ddi/ntddscsi/ni-ntddscsi-ioctl_scsi_miniport) IOCTL et le \_ \_ \_ \_ Code de contrôle 0x101 (CTLCODE ISCSITGT SPT session end) pour arrêter une session.</span><span class="sxs-lookup"><span data-stu-id="9f1b5-106">Used with the [**IOCTL\_SCSI\_MINIPORT**](/windows-hardware/drivers/ddi/ntddscsi/ni-ntddscsi-ioctl_scsi_miniport) IOCTL and the CTLCODE\_ISCSITGT\_SPT\_SESSION\_END (0x101) control code to stop a session.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f1b5-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9f1b5-107">Syntax</span></span>


```C++
typedef struct _ISCSITGT_SPT_SESSION_STOP {
  SRB_IO_CONTROL Header;
  SESSION_COOKIE ITNexusHandle;
} ISCSITGT_SPT_SESSION_STOP, *PISCSITGT_SPT_SESSION_STOP;
```



## <a name="members"></a><span data-ttu-id="9f1b5-108">Membres</span><span class="sxs-lookup"><span data-stu-id="9f1b5-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="9f1b5-109">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="9f1b5-109">**Header**</span></span>
</dt> <dd>

<span data-ttu-id="9f1b5-110">En-tête obligatoire.</span><span class="sxs-lookup"><span data-stu-id="9f1b5-110">Mandatory header.</span></span>

</dd> <dt>

<span data-ttu-id="9f1b5-111">**ITNexusHandle**</span><span class="sxs-lookup"><span data-stu-id="9f1b5-111">**ITNexusHandle**</span></span>
</dt> <dd>

<span data-ttu-id="9f1b5-112">Handle opaque représentant une session.</span><span class="sxs-lookup"><span data-stu-id="9f1b5-112">An opaque handle representing a session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9f1b5-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9f1b5-113">Requirements</span></span>



| <span data-ttu-id="9f1b5-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9f1b5-114">Requirement</span></span> | <span data-ttu-id="9f1b5-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="9f1b5-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="9f1b5-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9f1b5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9f1b5-117">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="9f1b5-117">None supported</span></span><br/>                               |
| <span data-ttu-id="9f1b5-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9f1b5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9f1b5-119">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9f1b5-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9f1b5-120">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="9f1b5-120">End of client support</span></span><br/>    | <span data-ttu-id="9f1b5-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="9f1b5-121">None supported</span></span><br/>                               |
| <span data-ttu-id="9f1b5-122">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="9f1b5-122">End of server support</span></span><br/>    | <span data-ttu-id="9f1b5-123">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="9f1b5-123">Windows Server 2012 R2</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="9f1b5-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f1b5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f1b5-125">Transfert de cible iSCSI</span><span class="sxs-lookup"><span data-stu-id="9f1b5-125">iSCSI Target Pass-Through</span></span>](/powershell/module/iscsi)
</dt> <dt>

[<span data-ttu-id="9f1b5-126">**\_contrôle d’e/s SRB \_**</span><span class="sxs-lookup"><span data-stu-id="9f1b5-126">**SRB\_IO\_CONTROL**</span></span>](/windows-hardware/drivers/ddi/ntddscsi/ns-ntddscsi-_srb_io_control)
</dt> </dl>

 

 
