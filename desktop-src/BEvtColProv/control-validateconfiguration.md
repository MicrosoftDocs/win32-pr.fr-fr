---
description: Validez un texte de configuration pour l’exactitude sans le définir comme actif. Retourne 1 en cas de réussite, 0 en cas d’erreur.
ms.assetid: baeabed0-7717-498a-9886-e49e4a101711
ms.tgt_platform: multiple
title: Méthode ValidateConfiguration de la classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.ValidateConfiguration
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: d4e1d0061b779a54973aeea1a487d8838781cf6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950405"
---
# <a name="validateconfiguration-method-of-the-control-class"></a>Méthode ValidateConfiguration de la classe Control

Validez un texte de configuration pour l’exactitude sans le définir comme actif. Retourne 1 en cas de réussite, 0 en cas d’erreur.

## <a name="syntax"></a>Syntaxe


```mof
Uint32 ValidateConfiguration(
  [in]  string Config,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Configuration* \[ de dans\]
</dt> <dd>

Configuration à vérifier.

</dd> <dt>

*ErrorString* \[ à\]
</dt> <dd>

Lorsque cette méthode est retournée, en cas d’erreur, ce paramètre contient une description de l’erreur de validation pour l’opération.

</dd> <dt>

*WarningString* \[ à\]
</dt> <dd>

Lorsque cette méthode est retournée, ce paramètre contient une description de tous les avertissements de validation pour l’opération.

Chaîne de texte avec des avertissements.

</dd> <dt>

*InfoString* \[ à\]
</dt> <dd>

Lorsque cette méthode est retournée, ce paramètre contient un ensemble d’informations sur la configuration.

</dd> <dt>

*ErrorType* \[ à\]
</dt> <dd>

Lorsque cette méthode est retournée, si une erreur de validation s’est produite, ce paramètre indique le type d’erreur.

Les valeurs possibles sont les suivantes :

<dt>

0
</dt> <dd>

L’argument est manquant.

</dd> <dt>

1
</dt> <dd>

Le format de l’argument n’est pas valide.

</dd> <dt>

2
</dt> <dd>

Un argument de configuration n’est pas valide.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

<dl> <dt>


</dt> <dd>

0

Échec

</dd> <dt>


</dt> <dd>

1

Succès

</dd> </dl>

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

 

 




