---
description: La méthode FormatText de l’objet record met en forme les champs en fonction du modèle dans le champ 0.
ms.assetid: 89a98b88-bb74-458c-a2df-727a8084145b
title: Record. FormatText, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.FormatText
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 377a1614d06ab4dfe1fa4f8b0745d420dc4d01ed
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127312262"
---
# <a name="recordformattext-method"></a>Record. FormatText, méthode

La méthode **FormatText** de l’objet [**Record**](record-object.md) met en forme les champs en fonction du modèle dans le champ 0.

## <a name="syntax"></a>Syntaxe


```JScript
Record.FormatText()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

La méthode **FormatText** suit les fonctionnalités de la fonction [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) si **MsiFormatRecord** a reçu un handle de programme d’installation null en tant que premier paramètre. Par conséquent, seuls les paramètres de champ d’enregistrement sont traités et les propriétés ne sont pas disponibles pour la substitution.

Par exemple, une chaîne telle que « mettre en forme ce champ : \[ 1 \] , mettre en forme cette propriété : \[ propriété \] » est résolue en « mettre en forme ce champ : valeur du champ 1, mettre en forme cette propriété : \[ propriété \] ».

Les paramètres qui doivent être [mis en forme](formatted.md) sont placés entre crochets \[ ... \] . Les crochets peuvent être itérés, car les substitutions sont résolues de l’intérieur vers l’extérieur.

Si une partie de la chaîne est entourée d’accolades {} et ne contient pas de crochets, elle reste inchangée, y compris les accolades.

Remarque dans le cas des [actions personnalisées d’exécution différée](deferred-execution-custom-actions.md), **FormatText** ne prend en charge qu’un ensemble limité de propriétés : les propriétés CustomActionData et ProductCode. Pour plus d’informations, consultez [obtention d’informations de contexte pour les actions personnalisées d’exécution différée](obtaining-context-information-for-deferred-execution-custom-actions.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iRecord est défini en tant que 000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)
</dt> <dt>

[Correct](formatted.md)
</dt> <dt>

[Types de données de colonne](column-data-types.md)
</dt> </dl>

 

 




