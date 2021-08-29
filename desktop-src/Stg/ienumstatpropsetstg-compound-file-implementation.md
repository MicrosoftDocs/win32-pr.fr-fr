---
title: Implémentation de fichiers IEnumSTATPROPSETSTG-Compound
description: L’implémentation de fichier composé de l’interface IEnumSTATPROPSETSTG est utilisée pour énumérer un tableau de structures STATPROPSETSTG qui contiennent des données de propriété statistiques.
ms.assetid: 1ce36e40-518c-411b-be5a-835a2dd0995e
keywords:
- IEnumSTATPROPSETSTG Strctd STG, implémentation de fichier composé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed34688f4967263649c828ab76b73b4d5150142ffa826e291fa4a0cfb7f50750
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663029"
---
# <a name="ienumstatpropsetstg-compound-file-implementation"></a>Implémentation de fichiers IEnumSTATPROPSETSTG-Compound

L’implémentation de fichier composé de l’interface [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) est utilisée pour énumérer un tableau de structures [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) qui contiennent des données de propriété statistiques. L’implémentation [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) gère les données statistiques et est associée à un objet de stockage de fichiers composés actuel.

## <a name="when-to-use"></a>Quand l’utiliser

Appelez les méthodes de [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) pour énumérer les structures [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) , chacune fournissant des données sur l’un des jeux de propriétés associés à l’objet de stockage de fichiers composés.

## <a name="remarks"></a>Remarques

<dl> <dt>

<span id="IEnumSTATPROPSETSTG__Next"></span><span id="ienumstatpropsetstg__next"></span><span id="IENUMSTATPROPSETSTG__NEXT"></span>[**IEnumSTATPROPSETSTG :: suivant**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dd>

Obtient le suivant d’une ou plusieurs structures [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) (le nombre est spécifié par le paramètre *celt* ). Les éléments **STATPROPSETSTG** fournis via un appel à l’implémentation de fichier composé de [**IEnumSTATPROPSETSTG :: Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) suivent les règles suivantes :

-   Si [**IEnumSTATPROPSETSTG :: Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) ne peut pas fournir STATPROPSETSTG. fmtid, les zéros sont écrits dans ce membre. Cela se produit lorsque le jeu de propriétés n’a pas de nom prédéfini (tel que \\ 005SummaryInformation) et qu’il ne s’agit pas d’une valeur légale.
-   Le jeu de propriétés DocumentSummaryInformation et UserDefined est spécial, car il peut avoir deux sections de jeu de propriétés. Ce jeu de propriétés est décrit dans la section [jeux de propriétés DocumentSummaryInformation et UserDefined](the-documentsummaryinformation-and-userdefined-property-sets.md). La deuxième section s’appelle les propriétés User-Defined. Chaque section est identifiée avec un identificateur de format unique (FMTID). Quand [**IPropertySetStorage :: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum) est utilisé pour énumérer des jeux de propriétés, le jeu de propriétés User-Defined n’est pas énuméré.

> [!Note]  
> Si vous créez toujours un jeu de propriétés à l’aide de [**IPropertySetStorage :: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create), alors, étant donné qu’un « GUID de caractère » est créé pour le nom de stockage, [**IEnumSTATPROPSETSTG :: Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) retourne un fmtid non nul et valide pour le jeu de propriétés \[ STATPROPSETSTG. fmtid \] .

 

-   Le membre STATPROPSETSTG. grfFlags ne reflète pas nécessairement si le jeu de propriétés est ANSI ou non. Si PROPSETFLAG \_ ANSI est défini, le jeu de propriétés est absolument ANSI. Si PROPSETFLAG \_ ANSI est Clear, le jeu de propriétés peut être Unicode ou non-Unicode, car il n’est pas possible de savoir s’il s’agit d’un ANSI sans l’ouvrir.
-   Le membre STATPROPSETSTG. grfFlags indique si le jeu de propriétés est simple ou non. par conséquent, le paramètre de l' \_ indicateur PROPSETFLAG non simple est toujours valide.
-   Si [**IEnumSTATPROPSETSTG :: Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) ne peut pas fournir STATPROPSETSTG. CLSID, il est défini sur tous les zéros (CLSID \_ null). Dans l’implémentation de fichier composé COM, cela se produit lorsque le jeu de propriétés est simple (l' \_ indicateur PROPSETFLAG non simple n’est pas défini) ou n’est pas simple, mais le CLSID n’a pas été défini explicitement. Pour les jeux de propriétés non simples, le CLSID reçu est celui qui est géré par le [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)sous-jacent.
-   Si [**IEnumSTATPROPSETSTG :: Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) ne peut pas fournir les champs d’heure \[ **ctime**, **mtime**, **atime** \] , chaque heure non prise en charge sera définie sur zéros. Dans l’implémentation de fichier composé COM, l’obtention de ces valeurs dépend de leur récupération de l’implémentation [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) sous-jacente.

</dd> <dt>

<span id="IEnumSTATPROPSETSTG__Skip"></span><span id="ienumstatpropsetstg__skip"></span><span id="IENUMSTATPROPSETSTG__SKIP"></span>[**IEnumSTATPROPSETSTG :: Skip**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> <dd>

Ignore le nombre d’éléments spécifiés dans *celt*. Retourne S \_ OK si le nombre d’éléments spécifié est ignoré, retourne la \_ valeur false si moins d’éléments que le nombre demandé sont ignorés. Dans tous les autres cas, retourne l’erreur appropriée.

</dd> <dt>

<span id="IEnumSTATPROPSETSTG__Reset"></span><span id="ienumstatpropsetstg__reset"></span><span id="IENUMSTATPROPSETSTG__RESET"></span>[**IEnumSTATPROPSETSTG :: Reset**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> <dd>

Définit le curseur au début de l’énumération. En cas de réussite, retourne S \_ OK ; sinon, retourne STG \_ E \_ INVALIDHANDLE.

</dd> <dt>

<span id="IEnumSTATPROPSETSTG__Clone"></span><span id="ienumstatpropsetstg__clone"></span><span id="IENUMSTATPROPSETSTG__CLONE"></span>[**IEnumSTATPROPSETSTG :: Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> <dd>

Copie l’état d’énumération actuel de cet énumérateur.

</dd> </dl>

 

 