---
title: Méthode IDWriteFont2 IsColorFont
description: Permet de déterminer si un chemin d’accès de rendu des couleurs est potentiellement nécessaire.
ms.assetid: E21BB773-923E-461B-B966-A186ACD0164A
keywords:
- Écriture directe de la méthode IsColorFont
- Méthode IsColorFont Write directe, interface IDWriteFont2
- Écriture directe de l’interface IDWriteFont2, méthode IsColorFont
topic_type:
- apiref
api_name:
- IDWriteFont2.IsColorFont
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 353499c5e1c00ae37e585ecc6be47e5a2033d795
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416936"
---
# <a name="idwritefont2iscolorfont-method"></a>IDWriteFont2 :: IsColorFont, méthode

Permet de déterminer si un chemin d’accès de rendu des couleurs est potentiellement nécessaire.

## <a name="syntax"></a>Syntaxe


```C++
BOOL IsColorFont();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Type : **bool**

Retourne la **valeur true** si la police contient des informations sur la couleur (tables colr et CPAL); Sinon, **false**.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | \[applications Windows 8.1 desktop apps \| UWP\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Server 2012 Applications de \[ Bureau R2 \| applications UWP\]<br/>                          |
| Téléphone minimal pris en charge<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]<br/> |
| Bibliothèque<br/>                  | <dl> <dt>DWrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDWriteFont2**](idwritefont2.md)
</dt> </dl>

 

 





