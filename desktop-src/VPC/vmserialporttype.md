---
title: Énumération VMSerialPortType (VPCCOMInterfaces. h)
description: Spécifie le type de port série.
ms.assetid: 1385292b-ee3c-41f0-805a-df126f33cabb
keywords:
- Virtual PC de l’énumération VMSerialPortType
topic_type:
- apiref
api_name:
- VMSerialPortType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca9b6171053e980f1f5dbdc52ef28deed177edba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508970"
---
# <a name="vmserialporttype-enumeration"></a><span data-ttu-id="8c2a6-104">Énumération VMSerialPortType</span><span class="sxs-lookup"><span data-stu-id="8c2a6-104">VMSerialPortType enumeration</span></span>

<span data-ttu-id="8c2a6-105">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8c2a6-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8c2a6-106">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8c2a6-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8c2a6-107">Spécifie le type de port série.</span><span class="sxs-lookup"><span data-stu-id="8c2a6-107">Specifies the type of serial port.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c2a6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8c2a6-108">Syntax</span></span>


```C++
typedef enum  { 
  vmSerialPort_HostPort   = 0,
  vmSerialPort_TextFile   = 1,
  vmSerialPort_NamedPipe  = 2,
  vmSerialPort_Null       = 3
} VMSerialPortType;
```



## <a name="constants"></a><span data-ttu-id="8c2a6-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="8c2a6-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8c2a6-110"><span id="vmSerialPort_HostPort"></span><span id="vmserialport_hostport"></span><span id="VMSERIALPORT_HOSTPORT"></span>**vmSerialPort \_ appelait hostport**</span><span class="sxs-lookup"><span data-stu-id="8c2a6-110"><span id="vmSerialPort_HostPort"></span><span id="vmserialport_hostport"></span><span id="VMSERIALPORT_HOSTPORT"></span>**vmSerialPort\_HostPort**</span></span>
</dt> <dd>

<span data-ttu-id="8c2a6-111">Port série hôte.</span><span class="sxs-lookup"><span data-stu-id="8c2a6-111">A host serial port.</span></span>

</dd> <dt>

<span data-ttu-id="8c2a6-112"><span id="vmSerialPort_TextFile"></span><span id="vmserialport_textfile"></span><span id="VMSERIALPORT_TEXTFILE"></span>**vmSerialPort \_ TextFile**</span><span class="sxs-lookup"><span data-stu-id="8c2a6-112"><span id="vmSerialPort_TextFile"></span><span id="vmserialport_textfile"></span><span id="VMSERIALPORT_TEXTFILE"></span>**vmSerialPort\_TextFile**</span></span>
</dt> <dd>

<span data-ttu-id="8c2a6-113">Fichier texte hôte.</span><span class="sxs-lookup"><span data-stu-id="8c2a6-113">A host text file.</span></span>

</dd> <dt>

<span data-ttu-id="8c2a6-114"><span id="vmSerialPort_NamedPipe"></span><span id="vmserialport_namedpipe"></span><span id="VMSERIALPORT_NAMEDPIPE"></span>**vmSerialPort \_ NamedPipe**</span><span class="sxs-lookup"><span data-stu-id="8c2a6-114"><span id="vmSerialPort_NamedPipe"></span><span id="vmserialport_namedpipe"></span><span id="VMSERIALPORT_NAMEDPIPE"></span>**vmSerialPort\_NamedPipe**</span></span>
</dt> <dd>

<span data-ttu-id="8c2a6-115">Canal nommé.</span><span class="sxs-lookup"><span data-stu-id="8c2a6-115">A named pipe.</span></span>

</dd> <dt>

<span data-ttu-id="8c2a6-116"><span id="vmSerialPort_Null"></span><span id="vmserialport_null"></span><span id="VMSERIALPORT_NULL"></span>**vmSerialPort \_ null**</span><span class="sxs-lookup"><span data-stu-id="8c2a6-116"><span id="vmSerialPort_Null"></span><span id="vmserialport_null"></span><span id="VMSERIALPORT_NULL"></span>**vmSerialPort\_Null**</span></span>
</dt> <dd>

<span data-ttu-id="8c2a6-117">Un port série **null** (ignore tous les bits qui lui sont envoyés).</span><span class="sxs-lookup"><span data-stu-id="8c2a6-117">A **NULL** serial port (discards all bits sent to it).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8c2a6-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c2a6-118">Requirements</span></span>



| <span data-ttu-id="8c2a6-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8c2a6-119">Requirement</span></span> | <span data-ttu-id="8c2a6-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c2a6-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c2a6-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c2a6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8c2a6-122">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8c2a6-122">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8c2a6-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c2a6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8c2a6-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c2a6-124">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8c2a6-125">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="8c2a6-125">End of client support</span></span><br/>    | <span data-ttu-id="8c2a6-126">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8c2a6-126">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8c2a6-127">Produit</span><span class="sxs-lookup"><span data-stu-id="8c2a6-127">Product</span></span><br/>                  | <span data-ttu-id="8c2a6-128">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8c2a6-128">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8c2a6-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="8c2a6-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c2a6-130"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c2a6-130"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c2a6-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c2a6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c2a6-132">**IVMSerialPort**</span><span class="sxs-lookup"><span data-stu-id="8c2a6-132">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> </dl>

 

