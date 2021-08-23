---
title: Clé d'interface
description: Inscrit les nouvelles interfaces en associant un nom d’interface à un ID d’interface (IID). Il doit y avoir une sous-clé IID pour chaque nouvelle interface.
ms.assetid: 2b2b7506-ac42-4bc4-bad5-17be57d6b4f5
keywords:
- Clé de registre de l’interface COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cda0cc29331521025a9274dca7b85080be2ddd5a9b631d2660eadaa13fe4941a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048147"
---
# <a name="interface-key"></a>Clé d'interface

Inscrit les nouvelles interfaces en associant un nom d’interface à un ID d’interface (IID). Il doit y avoir une sous-clé IID pour chaque nouvelle interface.

## <a name="registry-key"></a>Clé de Registre

**HKEY \_ \_Interface des \\ \\ classes de \\ logiciels de l’ordinateur local** \\ *{* IID *}*



| Valeur de Registre                               | Description                                                                                            |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**BaseInterface**](baseinterface.md)       | Identifie l’interface à partir de laquelle l’interface actuelle est dérivée.                                  |
| [**NumMethods**](nummethods.md)             | Contient le nombre de méthodes dans l’interface associée, y compris les méthodes des interfaces dérivées. |
| [**ProxyStubClsid**](proxystubclsid.md)     | Cartes un IID à un CLSID dans des dll proxy 16 bits.                                                           |
| [**ProxyStubClsid32**](proxystubclsid32.md) | Cartes un IID à un CLSID dans des dll de proxy 32 bits.                                                           |



 

## <a name="remarks"></a>Remarques

La clé de classes de logiciels de l' **\_ \_ ordinateur \\ \\ local HKEY** correspond à la clé **\_ \_ racine HKEY classes** , qui a été conservée pour la compatibilité avec les versions antérieures de com.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface**](interface.md)
</dt> </dl>

 

 




