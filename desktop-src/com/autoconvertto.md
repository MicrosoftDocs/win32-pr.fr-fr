---
title: AutoConvertTo
description: Spécifie la conversion automatique d’une classe d’objets donnée en une nouvelle classe d’objets.
ms.assetid: e34b799b-0d23-4034-ba79-49e92ec4dea7
keywords:
- Clé de Registre AutoConvertTo COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 160f6591ed318ad7622e0bf3c0af5187f95d3be3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127295758"
---
# <a name="autoconvertto"></a>AutoConvertTo

Spécifie la conversion automatique d’une classe d’objets donnée en une nouvelle classe d’objets.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      AutoConvertTo = value
```

## <a name="remarks"></a>Notes

Il s’agit d’une valeur de **reg \_ SZ** qui spécifie l’identificateur de classe de l’objet vers lequel l’objet ou la classe d’objets donné doit être converti.

Cette clé est généralement utilisée pour convertir automatiquement des fichiers créés par une version antérieure d’une application vers une version plus récente de l’application.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**OleDoAutoConvert**](/windows/desktop/api/Ole2/nf-ole2-oledoautoconvert)
</dt> <dt>

[**OleGetAutoConvert**](/windows/desktop/api/Ole2/nf-ole2-olegetautoconvert)
</dt> <dt>

[**OleSetAutoConvert**](/windows/desktop/api/Ole2/nf-ole2-olesetautoconvert)
</dt> </dl>

 

 




