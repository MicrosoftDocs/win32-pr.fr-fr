---
title: TreatAs
description: Spécifie le CLSID d’une classe qui peut émuler la classe actuelle.
ms.assetid: 1d7a1677-738a-4258-9afc-e77bd0dcf40f
keywords:
- Traiter la clé de registre COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc0808242b0732521bdd45a7b8fcdb65783ae83e5293f6c7fac39e51d50e609a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639319"
---
# <a name="treatas"></a>TreatAs

Spécifie le CLSID d’une classe qui peut émuler la classe actuelle.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      TreatAs = {CLSID_TreatAs}
```

## <a name="remarks"></a>Remarques

Il s’agit d’une valeur de **reg \_ SZ** .

L’émulation est la possibilité pour une application d’ouvrir et de modifier un objet d’une classe différente, tout en conservant le format d’origine de l’objet. La résolution se produit sur l’ordinateur local. par conséquent, dans le cas de l’activation à distance, la résolution se produit sur l’ordinateur client à l’aide du CLSID spécifié par **TreatAs**.

DCOM examine le registre local pour **traiteras**, même si vous appelez la fonction [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) et spécifiez un serveur distant. Cela signifie que si vous avez une entrée **TreatAs** pour Class1 à traiter comme Classe2 sur votre ordinateur local, mais que vous appelez **CoCreateInstance** pour créer une instance de Class1 et que vous spécifiez un serveur distant, DCOM tente de créer une instance de Class2 sur le serveur distant, même si Class2 n’est pas inscrit sur le serveur distant, ce qui entraîne l’échec de l’appel à **CoCreateInstance** .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Traitement autotraité**](autotreatas.md)
</dt> <dt>

[**CoGetTreatAsClass**](/windows/desktop/api/combaseapi/nf-combaseapi-cogettreatasclass)
</dt> <dt>

[**CoTreatAsClass**](/windows/desktop/api/Objbase/nf-objbase-cotreatasclass)
</dt> </dl>

 

 




