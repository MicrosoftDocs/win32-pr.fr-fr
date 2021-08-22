---
title: Interface IDWriteFont2
description: Représente une police physique dans une collection de polices.
ms.assetid: 4E3069AE-5882-4A26-A36D-BE7D7EE1B0C3
keywords:
- Écriture directe de l’interface IDWriteFont2
- Écriture directe de l’interface IDWriteFont2, décrite
topic_type:
- apiref
api_name:
- IDWriteFont2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fea5956c14a203020106fe6ecafdffb1522810d8f56684bbeafd158045444e34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071685"
---
# <a name="idwritefont2-interface"></a>Interface IDWriteFont2

Représente une police physique dans une collection de polices.

Cette interface ajoute la possibilité de vérifier si un chemin de rendu des couleurs est potentiellement nécessaire.

## <a name="members"></a>Membres

L’interface **IDWriteFont2** hérite de [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1). **IDWriteFont2** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IDWriteFont2** possède ces méthodes.



| Méthode                                          | Description                                                                        |
|:------------------------------------------------|:-----------------------------------------------------------------------------------|
| [**IsColorFont**](idwritefont2-iscolorfont.md) | Permet de déterminer si un chemin d’accès de rendu des couleurs est potentiellement nécessaire.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | \[applications Windows 8.1 desktop apps \| UWP\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Server 2012 Applications de \[ Bureau R2 \| applications UWP\]<br/>                          |
| Téléphone minimal pris en charge<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]<br/> |
| Bibliothèque<br/>                  | <dl> <dt>DWrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1)
</dt> </dl>

 

