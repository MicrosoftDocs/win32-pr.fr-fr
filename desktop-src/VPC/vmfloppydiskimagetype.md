---
title: Énumération VMFloppyDiskImageType (VPCCOMInterfaces. h)
description: Spécifie les formats de disquette.
ms.assetid: 7eb504c0-dfb7-45eb-a943-b453b5f8ca63
keywords:
- Virtual PC de l’énumération VMFloppyDiskImageType
topic_type:
- apiref
api_name:
- VMFloppyDiskImageType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b00daad9cf9abc0f713e5f3b5f530d2facd696b6f48bb17167b0d4ddecb76d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118591434"
---
# <a name="vmfloppydiskimagetype-enumeration"></a>Énumération VMFloppyDiskImageType

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Spécifie les formats de disquette.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum  { 
  vmFloppyDiskImage_Unknown                = 0,
  vmFloppyDiskImage_LowDensity             = 1,
  vmFloppyDiskImage_HighDensity            = 2,
  vmFloppyDiskImage_DMF                    = 3,
  vmFloppyDiskImage_LowDensitySingleSided  = 4,
  vmFloppyDiskImage_MediumDensity          = 5,
  vmFloppyDiskImage_HighDensityMSS         = 6
} VMFloppyDiskImageType;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="vmFloppyDiskImage_Unknown"></span><span id="vmfloppydiskimage_unknown"></span><span id="VMFLOPPYDISKIMAGE_UNKNOWN"></span>**vmFloppyDiskImage \_ inconnu**
</dt> <dd>

Format inconnu.

</dd> <dt>

<span id="vmFloppyDiskImage_LowDensity"></span><span id="vmfloppydiskimage_lowdensity"></span><span id="VMFLOPPYDISKIMAGE_LOWDENSITY"></span>**vmFloppyDiskImage \_ LowDensity**
</dt> <dd>

Format à faible densité (720K).

</dd> <dt>

<span id="vmFloppyDiskImage_HighDensity"></span><span id="vmfloppydiskimage_highdensity"></span><span id="VMFLOPPYDISKIMAGE_HIGHDENSITY"></span>**vmFloppyDiskImage \_ HighDensity**
</dt> <dd>

Un format à haute densité (1,44 Mo).

</dd> <dt>

<span id="vmFloppyDiskImage_DMF"></span><span id="vmfloppydiskimage_dmf"></span><span id="VMFLOPPYDISKIMAGE_DMF"></span>**\_DMF vmFloppyDiskImage**
</dt> <dd>

Un format de média de distribution (1.68 Mo).

</dd> <dt>

<span id="vmFloppyDiskImage_LowDensitySingleSided"></span><span id="vmfloppydiskimage_lowdensitysinglesided"></span><span id="VMFLOPPYDISKIMAGE_LOWDENSITYSINGLESIDED"></span>**vmFloppyDiskImage \_ LowDensitySingleSided**
</dt> <dd>

Format à faible densité à un seul côté.

</dd> <dt>

<span id="vmFloppyDiskImage_MediumDensity"></span><span id="vmfloppydiskimage_mediumdensity"></span><span id="VMFLOPPYDISKIMAGE_MEDIUMDENSITY"></span>**vmFloppyDiskImage \_ MediumDensity**
</dt> <dd>

Un format de densité moyenne (1,2 Mo).

</dd> <dt>

<span id="vmFloppyDiskImage_HighDensityMSS"></span><span id="vmfloppydiskimage_highdensitymss"></span><span id="VMFLOPPYDISKIMAGE_HIGHDENSITYMSS"></span>**vmFloppyDiskImage \_ HighDensityMSS**
</dt> <dd>

Une taille de secteur multiple à haute densité (MSS), utilisée par le format de distribution étendue (XDF).

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMVirtualPC::CreateFloppyDiskImage**](ivmvirtualpc-createfloppydiskimage.md)
</dt> <dt>

[**IVMVirtualPC::GetFloppyDiskImageType**](ivmvirtualpc-getfloppydiskimagetype.md)
</dt> </dl>

 

