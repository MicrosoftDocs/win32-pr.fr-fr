---
title: ProxyStubClsid32
description: Cartes un IID à un CLSID dans des dll de proxy 32 bits.
ms.assetid: 8d63d2b1-c8ba-4fe8-8025-e7ceee422ee7
keywords:
- Valeur de Registre ProxyStubClsid32 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d9098ffc7771d3f900489292694ade462a2214e733294a1ed18e6ddb9817692
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118309895"
---
# <a name="proxystubclsid32"></a>ProxyStubClsid32

Cartes un IID à un CLSID dans des dll de proxy 32 bits.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\Interface
   {IID}
      ProxyStubClsid32 = {CLSID}
```

## <a name="remarks"></a>Remarques

Il s’agit d’une valeur de **reg \_ SZ** qui spécifie le CLSID de l’IID.

Il s’agit d’une entrée obligatoire, car le mappage IID-à-CLSID peut être différent pour les interfaces 16 bits et 32 bits. Le mappage IID-to-CLSID dépend de la façon dont les proxies d’interface sont empaquetés dans un ensemble de dll proxy.

Si vous ajoutez des interfaces, vous devez utiliser cette entrée pour les inscrire (systèmes 32 bits) afin qu’OLE puisse trouver le code de communication à distance approprié pour établir la communication entre processus.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal)
</dt> <dt>

[**Interface**](interface-key.md)
</dt> <dt>

[**ProxyStubClsid**](proxystubclsid.md)
</dt> </dl>

 

 