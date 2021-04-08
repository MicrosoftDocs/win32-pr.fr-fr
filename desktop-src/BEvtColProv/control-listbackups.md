---
description: Retourne la liste des fichiers de configuration de sauvegarde enregistrés qui peuvent être restaurés.
ms.assetid: 9487c50e-ef3b-425f-92ef-0614290e9af4
ms.tgt_platform: multiple
title: Méthode ListBackups de la classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.ListBackups
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 858fb7ee38b7875426ae31172618ad8ac60510ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110059"
---
# <a name="listbackups-method-of-the-control-class"></a>Méthode ListBackups de la classe Control

Retourne la liste des fichiers de configuration de sauvegarde enregistrés qui peuvent être restaurés.

## <a name="syntax"></a>Syntaxe


```mof
void ListBackups(
  [out] Uint32 OriginalTimestampLow,
  [out] Uint32 OriginalTimestampHigh,
  [out] string Files[],
  [out] Uint32 FilesTimestampLow[],
  [out] Uint32 FilesTimestampHigh[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*OriginalTimestampLow* \[ à\]
</dt> <dd>

Horodateur de la définition de la configuration actuelle (si elle a été restaurée à partir d’une sauvegarde, contiendra l’horodateur d’origine). Il s’agit de la partie basse de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*OriginalTimestampHigh* \[ à\]
</dt> <dd>

Horodateur de la définition de la configuration actuelle (si elle a été restaurée à partir d’une sauvegarde, contiendra l’horodateur d’origine). Il s’agit de la partie haute de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*Fichiers* \[ à\]
</dt> <dd>

Liste des fichiers de sauvegarde disponibles, dans l’ordre, de la plus récente à la plus ancienne.

</dd> <dt>

*FilesTimestampLow* \[ à\]
</dt> <dd>

Pour chaque fichier de sauvegarde, horodatage de la définition de sa configuration. Il s’agit de la partie basse de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*FilesTimestampHigh* \[ à\]
</dt> <dd>

Pour chaque fichier de sauvegarde, horodatage de la définition de sa configuration. Il s’agit de la partie haute de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                                          |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                       |
| Espace de noms<br/>                | Racine \\ Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Contrôler**](control.md)
</dt> </dl>

 

