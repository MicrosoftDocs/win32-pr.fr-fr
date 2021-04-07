---
title: Architecture d’extension ADSI
description: Les extensions ADSI sont basées sur le modèle d’agrégation COM avec plusieurs améliorations. Les extensions doivent adhérer à toutes les règles COM. Pour plus d’informations, consultez la spécification COM.
ms.assetid: 59e39273-1f66-4bdd-89ed-31947a268d1f
ms.tgt_platform: multiple
keywords:
- extensions ADSI, architecture d’extension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 377409f4b9ac36d72d6885e89860b9e6e680b103
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730285"
---
# <a name="adsi-extension-architecture"></a>Architecture d’extension ADSI

Les extensions ADSI sont basées sur le modèle d’agrégation COM avec plusieurs améliorations. Les extensions doivent adhérer à toutes les règles COM. Pour plus d’informations, consultez la spécification COM.

Voici un aperçu du modèle d’agrégation COM.

![modèle d’agrégation com](images/comagmod.png)

Un agrégat, également connu sous le nom d’objet interne, est un objet créé par une agrégation. Votre objet d’extension est un agrégat.

Un agrégateur, également appelé objet externe, est un objet qui crée un agrégat. ADSI est une agrégation.

L’objet interne délègue son [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) à l' **IUnknown** de l’agrégateur.

Les extensions ADSI ajoutent les améliorations suivantes à l’agrégation COM pour répondre à ses exigences :

-   Permet à chaque enregistreur d’extension d’étendre des objets ADSI. Un enregistreur d’extensions peut inscrire son extension auprès d’ADSI et ne pas être affecté par l’existence d’autres extensions. Dans le modèle d’agrégation COM, l’agrégation doit avoir le CLSID de l’agrégat. ADSI assouplit cette exigence en faisant lui-même Office d’agrégation pour toutes les extensions. Par conséquent, au lieu de former une couche de composants imbriqués, les extensions sont au même niveau.
-   Autorise un objet, un IDispatch. La prise en charge d’Automation est l’une des fonctionnalités les plus importantes d’ADSI. La prise en charge de l’automatisation est obtenue, car ADSI prend en charge l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . Les rédacteurs d’extensions sont encouragés à prendre en charge l’interface **IDispatch** . Toutefois, il ne doit y avoir qu’une seule interface **IDispatch** sur un objet donné. ADSI intègre et collecte les nombreuses interfaces **IDispatch** de différentes extensions et les présente comme un **IDispatch** cohérent au contrôleur Automation. Chaque extension, quand elle est agrégée, doit réacheminer ses appels **IDispatch** vers le **IDISPATCH** fourni par ADSI.

Toutes ces solutions sont possibles en raison des services fournis par le gestionnaire d’objets ADSI, qui résident sur chaque fournisseur ADSI.

L’illustration suivante montre l’architecture du modèle d’extension ADSI.

![architecture du modèle d’extension ADSI](images/adsiexmo.png)

ADSI prend en charge deux niveaux d’extension :

-   Prise en charge de la liaison précoce. Il s’agit du premier niveau de l’extension. Une extension doit prendre en charge l’inscription et implémenter de nouvelles interfaces. Les consommateurs d’extension doivent utiliser des outils ou des hôtes de script qui prennent en charge la liaison précoce, par exemple Visual C++, Visual Basic.
-   Prise en charge de la liaison tardive. Cela se produit lorsqu’une extension satisfait à toutes les exigences de liaison précoce, et implémente une interface supplémentaire, [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension). Les implémenteurs d’extension peuvent utiliser n’importe quel outil qui fonctionne comme un contrôleur Automation, tel que Windows Script Host, Active Server pages ou HTML avec VBScript.

 

 