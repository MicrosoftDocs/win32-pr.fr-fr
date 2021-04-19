---
description: Spécifie si un flux s’exclut mutuellement avec d’autres flux du même type.
ms.assetid: 00a426ae-297c-4fcb-8132-d9c538bc9f1a
title: Attribut MF_SD_MUTUALLY_EXCLUSIVE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24e3604eb9424bb646766f57261f745c57e18f3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541875"
---
# <a name="mf_sd_mutually_exclusive-attribute"></a>\_ \_ Attribut mutuelle exclusif MF \_ SD

Spécifie si un flux s’exclut mutuellement avec d’autres flux du même type.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>S’applique à

[**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)

## <a name="remarks"></a>Notes

Si cet attribut a la **valeur true** (différent de zéro), le flux s’exclut mutuellement avec d’autres flux du même type, tels que des données audio ou vidéo, au sein de la même présentation. Par exemple, si un fichier AVI contient plusieurs flux audio, ceux-ci sont marqués comme s’excluant mutuellement, car un seul flux audio doit être lu en même temps.

La valeur par défaut est **FALSE**.

> [!Note]  
> Cet attribut n’est pas utilisé pour les fichiers ASF (Advanced Systems Format), qui offrent un moyen plus sophistiqué de représenter des critères d’exclusion mutuelle. Pour plus d’informations, consultez [**IMFASFMutualExclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion).

 

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 7 \[ Desktop Apps \| UWP\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]<br/>                     |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs du descripteur de flux](stream-descriptor-attributes.md)
</dt> </dl>

 

 




