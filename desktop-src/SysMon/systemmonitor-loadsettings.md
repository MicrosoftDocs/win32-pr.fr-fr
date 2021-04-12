---
title: Méthode SystemMonitor. LoadSettings
description: Ajoute les compteurs dans le fichier de modèle HTML au moniteur système.
ms.assetid: 3f88e590-df2b-4861-8ee6-a08f8742e6ad
keywords:
- Méthode LoadSettings SysMon
- Méthode LoadSettings SysMon, objet SystemMonitor
- Objet SystemMonitor SysMon, méthode LoadSettings
topic_type:
- apiref
api_name:
- SystemMonitor.LoadSettings
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e412ebfe97035c4847391a7cc9166cf512897bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384708"
---
# <a name="systemmonitorloadsettings-method"></a>Méthode SystemMonitor. LoadSettings

Ajoute les compteurs dans le fichier de modèle HTML au moniteur système.

## <a name="syntax"></a>Syntaxe


```VB
SystemMonitor.LoadSettings( _
  ByVal SettingsFileName As String _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*SettingsFileName* \[ dans\]
</dt> <dd>

Chaîne HTML qui spécifie les compteurs à ajouter au moniteur système.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Pour enregistrer les compteurs actuels dans le moniteur système dans un fichier HTML, appelez la méthode [**systemmonitor. SaveAs**](systemmonitor-saveas.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





