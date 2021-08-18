---
title: ProxyStubClsid
description: Cartes un IID à un CLSID dans des dll proxy 16 bits.
ms.assetid: 07e1e9de-e529-496c-b9f7-e7f799089f02
keywords:
- Valeur de Registre ProxyStubClsid COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93f86db768979a72d2d2f0b8c7a137d6b105f4a52d082ec50c6e78ba271fbca3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129991"
---
# <a name="proxystubclsid"></a>ProxyStubClsid

Cartes un IID à un CLSID dans des dll proxy 16 bits.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\Interface
   {IID}
      ProxyStubClsid = {CLSID}
```

## <a name="remarks"></a>Remarques

Il s’agit d’une valeur de **reg \_ SZ** qui spécifie le CLSID de l’IID.

Si vous ajoutez des interfaces, vous devez utiliser cette entrée pour les inscrire (systèmes 16 bits) afin qu’OLE puisse trouver le code de communication à distance approprié pour établir la communication entre processus.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface**](interface-key.md)
</dt> <dt>

[**ProxyStubClsid32**](proxystubclsid32.md)
</dt> </dl>

 

 




