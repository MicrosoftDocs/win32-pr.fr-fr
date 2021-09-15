---
description: Spécifie une stratégie de contrôle de plug-in locale.
ms.assetid: 2936F3C9-3BCB-452A-8C03-35D73A200CE2
title: Attribut MF_LOCAL_PLUGIN_CONTROL_POLICY (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd1bdaee17651cebfdc844bb5b6998907b1cd295
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413004"
---
# <a name="mf_local_plugin_control_policy-attribute"></a>\_Attribut de \_ stratégie de contrôle de plug-in local MF \_ \_

Spécifie une stratégie de contrôle de plug-in locale.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Notes

Affectez à cet attribut l’une des valeurs de la [**\_ stratégie de contrôle du plug-in \_ \_ MF**](/windows/desktop/api/mfobjects/ne-mfobjects-mf_plugin_control_policy) .

Cet attribut permet à l’application de spécifier une stratégie locale plus restrictive que la stratégie au niveau du processus configurée par [**IMFPluginControl**](/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs du type de média](media-type-attributes.md)
</dt> </dl>

 

 




