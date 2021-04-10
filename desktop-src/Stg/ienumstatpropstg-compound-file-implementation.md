---
title: Implémentation de fichiers IEnumSTATPROPSTG-Compound
description: L’implémentation de fichier composé de l’interface IEnumSTATPROPSTG est utilisée pour énumérer des propriétés, ce qui donne des structures STATPROPSTG, qui contiennent des données de propriété statistiques.
ms.assetid: 8fa536f4-cce6-47e4-a860-2f43e48fa469
keywords:
- IEnumSTATPROPSTG Strctd STG, implémentation de fichier composé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bbffce14016efdb4e2a77d60096b6776e6c2189
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941265"
---
# <a name="ienumstatpropstg-compound-file-implementation"></a>Implémentation de fichiers IEnumSTATPROPSTG-Compound

L’implémentation de fichier composé de l’interface [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) est utilisée pour énumérer des propriétés, ce qui donne des structures [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) , qui contiennent des données de propriété statistiques. L’implémentation de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) gère les données statistiques et est associée à un objet de stockage de fichiers composés actuel.

Le constructeur de l’implémentation COM de [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) crée une classe qui lit le jeu de propriétés entier et crée un tableau statique qui peut être partagé lorsque **IEnumSTATPROPSTG :: Clone** est appelé.

## <a name="when-to-use"></a>Quand l’utiliser

Appelez l’implémentation de fichier composé de [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) pour énumérer les structures [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) qui contiennent des données sur les propriétés dans le jeu de propriétés actuel. Quand vous utilisez l’implémentation de fichier composé des interfaces de stockage des propriétés, appelez [**IPropertyStorage :: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) pour retourner un pointeur vers **IEnumSTATPROPSTG** pour gérer l’objet de stockage de propriétés et les éléments qu’il contient.

## <a name="remarks"></a>Notes

<dl> <dt>

<span id="IEnumSTATPROPSTG__Next"></span><span id="ienumstatpropstg__next"></span><span id="IENUMSTATPROPSTG__NEXT"></span>[**IEnumSTATPROPSTG :: suivant**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dd>

Obtient le suivant d’une ou plusieurs structures [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) (le nombre est spécifié par le paramètre *celt* ). Retourne S \_ OK en cas de réussite.

</dd> <dt>

<span id="IEnumSTATPROPSTG__Skip"></span><span id="ienumstatpropstg__skip"></span><span id="IENUMSTATPROPSTG__SKIP"></span>[**IEnumSTATPROPSTG :: Skip**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dd>

Ignore le nombre d’éléments spécifiés dans *celt*. L’élément suivant à énumérer par le biais d’un appel à Next devient alors l’élément après les éléments ignorés. Retourne S \_ OK si les éléments *celt* ont été ignorés ; retourne la \_ valeur false si moins de *celt* Elements ont été ignorés.

</dd> <dt>

<span id="IEnumSTATPROPSTG__Reset"></span><span id="ienumstatpropstg__reset"></span><span id="IENUMSTATPROPSTG__RESET"></span>[**IEnumSTATPROPSTG :: Reset**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dd>

Définit le curseur au début de l’énumération. En cas de réussite, retourne S \_ OK ; sinon, retourne STG \_ E \_ INVALIDHANDLE.

</dd> <dt>

<span id="IEnumSTATPROPSTG__Clone"></span><span id="ienumstatpropstg__clone"></span><span id="IENUMSTATPROPSTG__CLONE"></span>[**IEnumSTATPROPSTG :: Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dd>

Utilise le constructeur pour le [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) pour créer une copie du tableau. Étant donné que la classe qui construit le tableau statique contient en fait l’objet, cette fonction ajoute principalement au décompte de références.

</dd> </dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dt>

[**IPropertyStorage :: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)
</dt> </dl>

 

 