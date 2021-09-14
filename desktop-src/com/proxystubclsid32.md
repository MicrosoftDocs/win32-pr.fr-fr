---
title: ProxyStubClsid32
description: Cartes un IID à un CLSID dans des dll de proxy 32 bits.
ms.assetid: 8d63d2b1-c8ba-4fe8-8025-e7ceee422ee7
keywords:
- Valeur de Registre ProxyStubClsid32 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7d1d70ad2deb4f747ecf57fd12f0707ac8b2b9d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126923147"
---
# <a name="proxystubclsid32"></a>ProxyStubClsid32

Cartes un IID à un CLSID dans des dll de proxy 32 bits.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\Interface
   {IID}
      ProxyStubClsid32 = {CLSID}
```

## <a name="remarks"></a>Notes

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

 

 