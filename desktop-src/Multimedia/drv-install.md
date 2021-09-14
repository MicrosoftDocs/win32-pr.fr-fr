---
title: Message DRV_INSTALL (mmsystem. h)
description: Avertit le pilote qui est en cours d’installation. Le pilote doit créer et initialiser toutes les clés et valeurs de Registre nécessaires et vérifier que les pilotes et le matériel de prise en charge sont installés et correctement configurés.
ms.assetid: 8ee7b30b-600b-49f3-93a7-8faa7b87cfd8
keywords:
- message DRV_INSTALL Windows Multimedia
topic_type:
- apiref
api_name:
- DRV_INSTALL
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c91c71a4cb65bfaffa07bf16e09bec0d16b7b4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127239808"
---
# <a name="drv_install-message"></a>Message d’installation de DRV \_

Avertit le pilote qui est en cours d’installation. Le pilote doit créer et initialiser toutes les clés et valeurs de Registre nécessaires et vérifier que les pilotes et le matériel de prise en charge sont installés et correctement configurés.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*
</dt> <dd>

Identificateur du pilote installable. Il s’agit de la même valeur que celle précédemment retournée par le pilote à partir du message de l' [**\_ ouverture du DRV**](drv-open.md) .

</dd> <dt>

<span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*
</dt> <dd>

Handle de l’instance du pilote installable.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Adresse d’une structure [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) ou **null**. Si une structure est fournie, elle contient les noms de la clé de Registre et la valeur associée au pilote.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne l’une des valeurs suivantes :



| Condition requise | Valeur |
|-----------------|--------------------------------------------------------------------------------------------|
| DRVCNF \_ OK      | L’installation a réussi ; aucune action supplémentaire n’est requise.                             |
| DRVCNF \_ Annuler  | L’installation a échoué..                                                                  |
| redémarrage de DRVCNF \_ | L’installation a réussi, mais elle ne prend effet qu’après le redémarrage du système. |



 

## <a name="remarks"></a>Remarques

Le paramètre *lParam1* n’est pas utilisé.

Certains pilotes installables ajoutent des informations de configuration à la valeur affectée à la valeur de registre associée au pilote.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Mmsystem. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Pilotes installables](installable-drivers.md)
</dt> <dt>

[Messages de pilote installables](installable-driver-messages.md)
</dt> </dl>

 

