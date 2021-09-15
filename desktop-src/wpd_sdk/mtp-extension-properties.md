---
description: Propriétés d’extension MTP
ms.assetid: 58fc8741-261a-4e63-9fd3-8f0ca05866ad
title: Propriétés d’extension MTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86a653d05285d62c7660bd914a785807a2341a01
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522952"
---
# <a name="mtp-extension-properties"></a>Propriétés d’extension MTP

Les propriétés décrivent les objets, les propriétés, les ressources et les périphériques.

## <a name="vendor-extended-object-properties"></a>Fournisseur-propriétés de l’objet étendu

Quand un fabricant de périphériques crée une propriété étendue par un fournisseur pour un objet périphérique, il combine les **Propriétés wpd GUID du \_ fournisseur MTP de l' \_ \_ \_ \_ objet étendu \_** avec le code de propriété de l’objet pour construire une structure **PROPERTYKEY** .

Par exemple, si le code de propriété de l’objet est 0xD801, la **PROPERTYKEY** résultante serait comme indiqué dans l’exemple suivant :


```C++
{4D545058-4FCE-4578-95C8-8698A9BC0F49}\D801
```



## <a name="vendor-extended-device-properties"></a>Fournisseur-propriétés de l’appareil étendues

Quand un fabricant de périphériques crée une propriété étendue par un fournisseur pour un appareil, il combine les **Propriétés wpd GUID des \_ propriétés d' \_ \_ \_ \_ appareils \_ étendus du fournisseur MTP** avec le code de propriété de l’objet pour construire une structure **PROPERTYKEY** .

Par exemple, si le code de propriété de l’objet est 0xD001, la **PROPERTYKEY** résultante serait comme indiqué dans l’exemple suivant :


```C++
{4D545058-8900-40b3-8F1D-DC246E1E8370}\D001
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en charge des extensions MTP](supporting-mtp-extensions.md)
</dt> </dl>

 

 



