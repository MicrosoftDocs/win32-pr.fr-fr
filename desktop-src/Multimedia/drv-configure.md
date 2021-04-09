---
title: Message DRV_CONFIGURE (mmsystem. h)
description: Indique au pilote installable d’afficher sa boîte de dialogue de configuration et de permettre à l’utilisateur de spécifier de nouveaux paramètres pour l’instance de pilote d’installation donnée.
ms.assetid: 0d99fad7-ce79-4574-9fd8-262f7e758866
keywords:
- Message DRV_CONFIGURE Windows Multimedia
topic_type:
- apiref
api_name:
- DRV_CONFIGURE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30a761e7bda7188e93b02e436f2e952bed61bee9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942829"
---
# <a name="drv_configure-message"></a>DRV \_ configurer le message

Indique au pilote installable d’afficher sa boîte de dialogue de configuration et de permettre à l’utilisateur de spécifier de nouveaux paramètres pour l’instance de pilote d’installation donnée.

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

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Handle de la fenêtre parente. Cette fenêtre est utilisée comme fenêtre parente pour la boîte de dialogue de configuration.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Adresse d’une structure [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) ou **null**. Si la structure est donnée, elle contient les noms de la clé de Registre et la valeur associée au pilote.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne l’une des valeurs suivantes :



| Condition requise | Valeur |
|-----------------|----------------------------------------------------------------------------------------------------|
| DRVCNF \_ OK      | La configuration a réussi ; aucune action supplémentaire n’est requise.                                    |
| DRVCNF \_ Annuler  | L’utilisateur a annulé la boîte de dialogue ; aucune action supplémentaire n’est requise.                                   |
| redémarrage de DRVCNF \_ | La configuration est réussie, mais les modifications ne prennent effet qu’après le redémarrage du système. |



 

## <a name="remarks"></a>Notes

Certains pilotes installables ajoutent des informations de configuration à la valeur affectée à la valeur de registre associée au pilote.

Les valeurs de retour de DRV \_ Cancel, DRV \_ OK et DRV \_ restart sont obsolètes. elles ont été remplacées par DRVCNF \_ Cancel, DRVCNF \_ OK et DRVCNF \_ Restart, respectivement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>MMSYSTEM. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Pilotes installables](installable-drivers.md)
</dt> <dt>

[Messages de pilote installables](installable-driver-messages.md)
</dt> </dl>

 

