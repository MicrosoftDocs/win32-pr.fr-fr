---
description: Réinitialiser la configuration active du collecteur à partir du fichier de sauvegarde ultérieur (déterminé par la progression à partir de l’horodatage d’origine actuel). Si la configuration a été annulée, cela signifie que la modification n’a pas été effectuée.
ms.assetid: bd153ea3-9148-4e65-a44e-3f9fa1855f2f
ms.tgt_platform: multiple
title: Méthode Redo de la classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.Redo
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 45f8d2c8ae34ae3f045a579cbb588f1a67e635077951c10916655788b48f7795
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119579509"
---
# <a name="redo-method-of-the-control-class"></a>Méthode Redo de la classe Control

Réinitialiser la configuration active du collecteur à partir du fichier de sauvegarde ultérieur (déterminé par la progression à partir de l’horodatage d’origine actuel). Si la configuration a été annulée, cela signifie que la modification n’a pas été effectuée.

## <a name="syntax"></a>Syntaxe


```mof
Uint32 Redo(
  [in]  Uint32 OldTimestampLow,
  [in]  Uint32 OldTimestampHigh,
  [out] Uint32 NewTimestampLow,
  [out] Uint32 NewTimestampHigh,
  [out] Uint32 OriginalTimestampLow,
  [out] Uint32 OriginalTimestampHigh,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*OldTimestampLow* \[ dans\]
</dt> <dd>

Horodateur de la définition de la configuration précédente. Si la valeur est égale à 0, active la vérification de l’atomicité : la nouvelle configuration est appliquée uniquement si l’horodateur de l’ancienne configuration correspond (c.-à-d. que la configuration n’a pas été modifiée dans between). Il s’agit de la partie basse de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*OldTimestampHigh* \[ dans\]
</dt> <dd>

Horodateur de la définition de la configuration précédente. Si la valeur est égale à 0, active la vérification de l’atomicité : la nouvelle configuration est appliquée uniquement si l’horodateur de l’ancienne configuration correspond (c.-à-d. que la configuration n’a pas été modifiée dans between). Il s’agit de la partie haute de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*NewTimestampLow* \[ à\]
</dt> <dd>

Horodateur de la définition de la nouvelle configuration, si l’appel a échoué. Il s’agit de la partie basse de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*NewTimestampHigh* \[ à\]
</dt> <dd>

Horodateur de la définition de la nouvelle configuration, si l’appel a échoué. Il s’agit de la partie haute de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*OriginalTimestampLow* \[ à\]
</dt> <dd>

Horodateur d’origine de lorsque la configuration restaurée a été définie pour la première fois. Il s’agit de la partie basse de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*OriginalTimestampHigh* \[ à\]
</dt> <dd>

Horodateur d’origine de lorsque la configuration restaurée a été définie pour la première fois. Il s’agit de la partie haute de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*ErrorString* \[ à\]
</dt> <dd>

Chaîne de texte avec une explication de l’erreur.

</dd> <dt>

*WarningString* \[ à\]
</dt> <dd>

Chaîne de texte avec des avertissements.

</dd> <dt>

*InfoString* \[ à\]
</dt> <dd>

Chaîne de texte contenant des informations sur la configuration.

</dd> <dt>

*ErrorType* \[ à\]
</dt> <dd>

Type de l'erreur. Notez que 0 ou absent indique une réussite.

<dt>

0
</dt> <dd>

Réussite.

</dd> <dt>

1
</dt> <dd>

format d’argument incorrect

</dd> <dt>

2
</dt> <dd>

valeur d’argument incorrecte

</dd> <dt>

3
</dt> <dd>

erreur d’ouverture de ressource (Socket)

</dd> <dt>

4
</dt> <dd>

erreur de persistance (écriture de fichier)

</dd> <dt>

5
</dt> <dd>

erreur d’atomicité (l’ancien horodatage ne correspond pas)

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
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                                          |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                       |
| Espace de noms<br/>                | racine \\ Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Contrôler**](control.md)
</dt> </dl>

 

