---
title: ProxyStubClsid
description: Cartes un IID à un CLSID dans des dll proxy 16 bits.
ms.assetid: 07e1e9de-e529-496c-b9f7-e7f799089f02
keywords:
- Valeur de Registre ProxyStubClsid COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9adfbe319903b2e278be342d169a2e523c952693
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126923152"
---
# <a name="proxystubclsid"></a>ProxyStubClsid

Cartes un IID à un CLSID dans des dll proxy 16 bits.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\Interface
   {IID}
      ProxyStubClsid = {CLSID}
```

## <a name="remarks"></a>Notes

Il s’agit d’une valeur de **reg \_ SZ** qui spécifie le CLSID de l’IID.

Si vous ajoutez des interfaces, vous devez utiliser cette entrée pour les inscrire (systèmes 16 bits) afin qu’OLE puisse trouver le code de communication à distance approprié pour établir la communication entre processus.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface**](interface-key.md)
</dt> <dt>

[**ProxyStubClsid32**](proxystubclsid32.md)
</dt> </dl>

 

 




