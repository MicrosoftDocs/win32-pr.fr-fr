---
description: L’objet de données est central pour tous les transferts de données de Shell.
ms.assetid: c63d339e-ac62-4da1-b5ce-22d45a6a3413
title: Objet de données de Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de7c05810e3f641b5216d0923fef9798773678683f7f8c8af5cb90389f794da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119444039"
---
# <a name="shell-data-object"></a>Objet de données de Shell

L’objet de données est central pour tous les transferts de données de Shell. Il s’agit principalement d’un conteneur pour stocker les données transférées. Toutefois, la cible peut également communiquer avec l’objet de données pour faciliter certains types spécialisés de transfert de données de Shell, tels que les déplacements optimisés. Cette rubrique fournit une présentation générale de la façon dont les objets de données de Shell fonctionnent, de la façon dont ils sont construits par une source et de la façon dont ils sont gérés par une cible. Pour plus d’informations sur l’utilisation des objets de données pour transférer différents types de données de Shell, consultez Gestion des scénarios de Transfert de données de l' [interpréteur](datascenarios.md)de commandes.

-   [Fonctionnement des objets de données](#how-data-objects-work)
    -   [Formats du presse-papiers](#clipboard-formats)
    -   [FORMATETC, structure](#formatetc-structure)
    -   [STGMEDIUM, structure](#stgmedium-structure)
-   [Comment une source crée un objet de données](#how-a-source-creates-a-data-object)
    -   [Comment ajouter un objet de mémoire global à un objet de données](#how-to-add-a-global-memory-object-to-a-data-object)
    -   [Implémentation de IDataObject](#implementing-idataobject)
    -   [Implémentation de IDropSource](#implementing-idropsource)
-   [Comment une cible gère un objet de données](#how-a-target-handles-a-data-object)
    -   [Extraction des données de l’interpréteur de commandes à partir d’un objet de données](#extracting-shell-data-from-a-data-object)
    -   [Implémentation de IDropTarget](#implementing-idroptarget)
-   [Utilisation de l’objet d’assistance par glisser-déplacer](#using-the-drag-and-drop-helper-object)
    -   [Utilisation de l’interface IDragSourceHelper](#using-the-idragsourcehelper-interface)
    -   [Utilisation de l’interface IDropTargetHelper](#using-the-idroptargethelper-interface)

## <a name="how-data-objects-work"></a>Fonctionnement des objets de données

Les objets de données sont des objets COM (Component Object Model), créés par la source de données pour transférer des données vers une cible. Ils contiennent généralement plus d’un élément de données. Il existe deux raisons pour cette pratique :

-   Bien que presque n’importe quel type de données puisse être transféré avec un objet de données, la source ne connaît généralement pas le type de données que la cible peut accepter. Par exemple, les données peuvent être une partie d’un document texte mis en forme. Alors que la cible peut être en mesure de gérer des informations de mise en forme complexes, elle peut également être en mesure d’accepter uniquement du texte ANSI. Pour cette raison, les objets de données incluent souvent les mêmes données dans différents formats. La cible peut ensuite extraire les données dans un format qu’elle peut gérer.
-   Les objets de données peuvent également contenir des éléments de données auxiliaires qui ne sont pas des versions de données sources. Ce type d’élément de données fournit généralement des informations supplémentaires sur l’opération de transfert de données. Par exemple, l’interpréteur de commandes utilise des éléments de données auxiliaires pour indiquer si un fichier doit être copié ou déplacé.

### <a name="clipboard-formats"></a>Formats du presse-papiers

Chaque élément de données dans un objet de données est associé à un format, généralement appelé *format de presse-papiers*. Il existe un certain nombre de formats de presse-papiers standard, déclarés dans winuser. h, qui correspondent aux types de données couramment utilisés. Les formats de presse-papiers sont des entiers, mais ils sont normalement désignés par leur nom équivalent, qui se présente sous la forme CF \_ *xxx*. Par exemple, le format de presse-papiers pour le texte ANSI est \_ texte cf.

Les applications peuvent étendre la plage des formats de presse-papiers disponibles en définissant des formats privés. Pour définir un format privé, une application appelle [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata) avec une chaîne qui identifie le format. L’entier non signé retourné par la fonction est une valeur de format valide qui peut être utilisée comme un format de presse-papiers standard. Toutefois, la source et la cible doivent inscrire le format pour pouvoir l’utiliser. À une exception près :[CF \_ HDROP](clipboard.md): les formats de presse-papiers utilisés pour transférer les données de l’interpréteur de commandes sont définis en tant que formats privés. Ils doivent être inscrits par la source et la cible avant de pouvoir être utilisés. Pour obtenir une description des formats de presse-papiers de l’interpréteur de commandes disponibles, consultez formats du presse-papiers de Shell.

Bien qu’il existe quelques exceptions, les objets de données contiennent normalement un seul élément de données pour chaque format de presse-papiers qu’ils prennent en charge. Cette corrélation un-à-un entre le format et les données permet d’utiliser la valeur de format comme identificateur pour l’élément de données associé. En fait, lorsque vous discutez du contenu d’un objet de données, un élément de données particulier est généralement appelé « format » et est référencé par son nom de format. Par exemple, les expressions telles que « extraire le \_ format de texte cf... » sont généralement utilisés lors de l’étude d’un élément de données texte ANSI d’un objet de données.

Lorsque la cible de déplacement reçoit le pointeur vers l’objet de données, la cible de déplacement énumère les formats disponibles afin de déterminer quels types de données sont disponibles. Il demande ensuite un ou plusieurs des formats disponibles et extrait les données. La façon dont la cible extrait les données de l’interpréteur de commandes à partir d’un objet de données varie en fonction du format ; ce sujet est abordé en détail dans [la manière dont une cible gère un objet de données](#how-a-target-handles-a-data-object).

Avec les transferts de données du presse-papiers simples, les données sont placées dans un objet mémoire global. L’adresse de cet objet est placée dans le presse-papiers, en même temps que son format. Le format du presse-papiers indique à la cible le type de données qu’elle trouvera à l’adresse associée. Bien que les transferts de presse-papiers simples soient faciles à implémenter :

-   Les objets de données offrent un moyen bien plus souple de transférer des données.
-   Les objets de données sont mieux adaptés au transfert de grandes quantités de données.
-   Les objets de données doivent être utilisés pour transférer des données à l’aide d’une opération de glisser-déplacer.

Pour ces raisons, tous les transferts de données de Shell utilisent des objets de données. Avec les objets de données, les formats de presse-papiers ne sont pas utilisés directement. Au lieu de cela, les éléments de données sont identifiés avec une généralisation du format du presse-papiers, une structure [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) .

### <a name="formatetc-structure"></a>FORMATETC, structure

La structure [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) est une version étendue d’un format de presse-papiers. Utilisé pour les transferts de données de Shell, la structure **FORMATETC** présente les caractéristiques suivantes :

-   Un élément de données est toujours identifié par son format de presse-papiers, dans le membre **cfFormat** .
-   Le transfert de données n’est pas limité aux objets mémoire globaux. Le membre **TYMED** est utilisé pour indiquer le mécanisme de transfert de données contenu dans la structure [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) associée. Elle est définie sur l’une des valeurs [**TYMED \_ xxx**](/windows/win32/api/objidl/ne-objidl-tymed) .
-   L’interpréteur de commandes utilise le membre **Lindex** avec son format [CFSTR \_ FILECONTENTS](clipboard.md) pour permettre à un objet de données de contenir plus d’un élément de données par format. Pour plus d’informations sur l’utilisation de ce format, consultez la section *utilisation du \_ format CFSTR FILECONTENTS pour extraire des données d’un fichier dans* [gestion des scénarios de Shell transfert de données](datascenarios.md).
-   Le membre **dwAspect** est généralement défini sur le \_ contenu DVASPECT. Toutefois, il existe trois valeurs définies dans shlobj. h qui peuvent être utilisées pour le transfert de données d’interpréteur de commandes. 

    | Valeur               | Description                                                                                       |
    |---------------------|---------------------------------------------------------------------------------------------------|
    | \_copie DVASPECT      | Permet d’indiquer que le format représente une copie des données.                                   |
    | \_lien DVASPECT      | Permet d’indiquer que le format représente un raccourci vers les données.                               |
    | DVASPECT \_ ShortName | Utilisé avec le \_ format CF HDROP pour demander un chemin d’accès de fichier dont les noms sont abrégés au format 8,3. |

    

     

-   Le membre **PTD** n’est pas utilisé pour les transferts de données Shell et prend normalement la valeur **null**.

### <a name="stgmedium-structure"></a>STGMEDIUM, structure

La structure [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) donne accès aux données en cours de transfert. Trois mécanismes de transfert de données sont pris en charge pour les données de l’interpréteur de commandes :

-   Objet de mémoire global.
-   Une interface [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) .
-   Interface [**IStorage**](/windows/win32/api/objidl/nn-objidl-istorage) .

Le membre **TYMED** de la structure [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) est une valeur [**TYMED \_ xxx**](/windows/win32/api/objidl/ne-objidl-tymed) qui identifie le mécanisme de transfert de données. Le deuxième membre est un pointeur qui est utilisé par la cible pour extraire les données. Le pointeur peut être l’un des différents types, en fonction de la valeur **TYMED** . Les trois valeurs **TYMED** utilisées pour les transferts de données de Shell sont résumées dans le tableau ci-dessous, avec le nom de membre **STGMEDIUM** correspondant.



| Valeur TYMED     | Nom du membre | Description                                                                                                                                                                                                                                                                                                       |
|-----------------|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TYMED \_ HGLOBAL  | **hGlobal** | Pointeur vers un objet de mémoire global. Ce type de pointeur est généralement utilisé pour transférer de petites quantités de données. Par exemple, l’interpréteur de commandes utilise des objets mémoire globaux pour transférer des chaînes de texte courtes, telles que des noms de fichiers ou des URL.                                                                                    |
| TYMED \_ ISTREAM  | **pstm**    | Pointeur vers une interface [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) . Ce type de pointeur est recommandé pour la plupart des transferts de données Shell, car il requiert relativement peu de mémoire par rapport à TYMED \_ HGLOBAL. En outre, le \_ mécanisme de transfert de données TYMED ISTREAM ne requiert pas que la source stocke ses données d’une manière particulière. |
| TYMED, \_ ISTORAGE | **pstg**    | Pointeur vers une interface [**IStorage**](/windows/win32/api/objidl/nn-objidl-istorage) . La cible appelle les méthodes d’interface pour extraire les données. Comme TYMED \_ ISTREAM, ce type de pointeur requiert relativement peu de mémoire. Toutefois, étant donné que TYMED \_ ISTORAGE est moins souple que TYMED \_ ISTREAM, ce n’est pas aussi souvent utilisé.                  |



 

## <a name="how-a-source-creates-a-data-object"></a>Comment une source crée un objet de données

Lorsqu’un utilisateur lance un transfert de données de Shell, la source est chargée de créer un objet de données et de le charger avec des données. La procédure suivante résume le processus :

1.  Appelez [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata) pour obtenir une valeur de format de presse-papiers valide pour chaque format de Shell qui sera inclus dans l’objet de données. N’oubliez pas que [CF \_ HDROP](clipboard.md) est déjà un format de presse-papiers valide et qu’il n’est pas nécessaire de l’inscrire.
2.  Pour chaque format à transférer, vous pouvez placer les données associées dans un objet de mémoire global ou créer un objet qui fournit l’accès à ces données via une interface [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) ou [**IStorage**](/windows/win32/api/objidl/nn-objidl-istorage) . Les interfaces **IStream** et **IStorage** sont créées à l’aide de techniques com standard. Pour plus d’informations sur la gestion des objets mémoire globaux, consultez [Ajout d’un objet mémoire global à un objet de données](#how-to-add-a-global-memory-object-to-a-data-object).
3.  Créez des structures [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) et [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) pour chaque format.
4.  Instanciez un objet de données.
5.  Chargez les données dans l’objet de données en appelant la méthode [**IDataObject :: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) pour chaque format pris en charge et en passant les structures [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) et [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) du format.
6.  Avec les transferts de données du presse-papiers, appelez [**OleSetClipboard**](/windows/win32/api/ole2/nf-ole2-olesetclipboard) pour placer un pointeur vers l’interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) de l’objet de données dans le presse-papiers. Pour les transferts par glisser-déplacer, lancez une *boucle de glissement* en appelant [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop). Le pointeur **IDataObject** est passé à la cible de déplacement lorsque les données sont supprimées, ce qui met fin à la boucle de glissement.

L’objet de données est maintenant prêt à être transféré à la cible. Pour les transferts de données du presse-papiers, l’objet est simplement maintenu jusqu’à ce que la cible le demande en appelant [**OleGetClipboard**](/windows/win32/api/ole2/nf-ole2-olegetclipboard). Pour les transferts de données par glisser-déplacer, l’objet de données est chargé de créer une icône pour représenter les données et de les déplacer lorsque l’utilisateur déplace le curseur. Lorsque l’objet se trouve dans la boucle de glissement, la source reçoit les informations d’état via son interface [**IDropSource**](/windows/win32/api/oleidl/nn-oleidl-idropsource) . Pour plus d’informations, consultez [implémentation de IDropSource](#implementing-idropsource).

La source ne reçoit aucune notification si l’objet de données est récupéré à partir du presse-papiers par une cible. Lorsqu’un objet est supprimé sur une cible par une opération de glisser-déplacer, la fonction [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) qui a été appelée pour initier la boucle de glissement retourne.

### <a name="how-to-add-a-global-memory-object-to-a-data-object"></a>Comment ajouter un objet de mémoire global à un objet de données

La plupart des formats de données de Shell se présentent sous la forme d’un objet de mémoire globale. Utilisez la procédure suivante pour créer un format contenant un objet mémoire global et le charger dans l’objet de données :

1.  Créer une structure [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) . Définissez le membre **cfFormat** sur la valeur de format du presse-papiers appropriée et le membre **TYMED** sur TYMED \_ HGLOBAL.
2.  Créer une structure [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) . Définissez le membre **TYMED** sur TYMED \_ HGLOBAL.
3.  Créez un objet de mémoire globale en appelant [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc) pour allouer un bloc de mémoire de taille appropriée.
4.  Affectez le bloc de données à transférer à l’adresse renvoyée par [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc).
5.  Assignez l’adresse de l’objet mémoire globale au membre **hGlobal** de la structure [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) .
6.  Chargez le format dans l’objet de données en appelant [**IDataObject :: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) et en passant les structures [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) et [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) créées dans les étapes précédentes.

L’exemple de fonction suivant crée un objet mémoire global contenant une valeur **DWORD** et le charge dans un objet de données. Le paramètre **pdtobj** est un pointeur vers l’interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) de l’objet de données, **CF** correspond à la valeur du format du presse-papiers et **DW** à la valeur des données.


```C++
STDAPI DataObj_SetDWORD(IDataObject *pdtobj, UINT cf, DWORD dw)
{
    FORMATETC fmte = {(CLIPFORMAT) cf, 
                      NULL, 
                      DVASPECT_CONTENT, 
                      -1, 
                      TYMED_HGLOBAL};
    STGMEDIUM medium;

    HRESULT hres = E_OUTOFMEMORY;
    DWORD *pdw = (DWORD *)GlobalAlloc(GPTR, sizeof(DWORD));
    
    if (pdw)
    {
        *pdw = dw;       
        medium.tymed = TYMED_HGLOBAL;
        medium.hGlobal = pdw;
        medium.pUnkForRelease = NULL;

        hres = pdtobj->SetData(&fmte, &medium, TRUE);
 
        if (FAILED(hres))
            GlobalFree((HGLOBAL)pdw);
    }
    return hres;
}
```



### <a name="implementing-idataobject"></a>Implémentation de IDataObject

[**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) est l’interface principale d’un objet de données. Elle doit être implémentée par tous les objets de données. Elle est utilisée à la fois par la source et la cible à diverses fins, notamment :

-   Chargement des données dans l’objet de données.
-   Extraction des données de l’objet de données.
-   Détermination des types de données dans l’objet de données.
-   Fournir des commentaires à l’objet de données au résultat du transfert de données.

[**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) prend en charge un certain nombre de méthodes. Cette section explique comment implémenter les trois méthodes les plus importantes pour les objets de données Shell, [SetData](#setdata-method), [EnumFormatEtc](#enumformatetc-method)et [GetData](#getdata-method). Pour plus d’informations sur les autres méthodes, consultez la référence **IDataObject** .

### <a name="setdata-method"></a>SetData (méthode)

La fonction principale de la méthode [**IDataObject :: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) est de permettre à la source de charger des données dans l’objet de données. Pour chaque format à inclure, la source crée une structure [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) pour identifier le format et une structure [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) pour contenir un pointeur vers les données. La source appelle ensuite la méthode **IDataObject :: SetData** de l’objet et passe dans les structures **FORMATETC** et **STGMEDIUM** du format. La méthode doit stocker ces informations afin qu’elles soient disponibles lorsque la cible appelle [**IDataObject :: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) pour extraire les données de l’objet.

Toutefois, lors du transfert de fichiers, l’interpréteur de commandes place souvent les informations de chaque fichier à transférer dans un format [CFSTR \_ FILECONTENTS](clipboard.md) distinct. Pour distinguer les différents fichiers, le membre **Lindex** de la structure [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) de chaque fichier est défini sur une valeur d’index qui identifie le fichier particulier. Votre implémentation de [**IDataObject :: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) doit être capable de stocker plusieurs \_ formats CFSTR FILECONTENTS qui diffèrent uniquement par leurs membres **Lindex** .

Lorsque le curseur se trouve sur la fenêtre cible, la cible peut utiliser l' [objet d’assistance glisser-déplacer](#using-the-drag-and-drop-helper-object) pour spécifier l’image de glissement. L’objet d’assistance par glisser-déplacer appelle [**IDataObject :: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) pour charger des formats privés dans l’objet de données utilisé pour la prise en charge inter-processus. Pour prendre en charge l’objet d’assistance par glisser-déplacer, votre implémentation de **IDataObject :: SetData** doit être en mesure d’accepter et de stocker des formats privés arbitraires.

Une fois que les données ont été supprimées, certains types de transferts de données de Shell requièrent que la cible appelle [**IDataObject :: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) pour fournir à l’objet de données des informations sur le résultat de l’opération de déplacement. Par exemple, lors du déplacement de fichiers avec une opération de déplacement optimisée, la cible supprime normalement les fichiers d’origine, mais cela n’est pas obligatoire. La cible informe l’objet de données s’il a supprimé les fichiers en appelant **IDataObject :: SetData** avec un format [CFSTR \_ LOGICALPERFORMEDDROPEFFECT](clipboard.md) . Plusieurs autres formats de l' [interpréteur](clipboard.md) de commandes sont également utilisés par la cible pour transmettre des informations à l’objet de données. Votre implémentation de **IDataObject :: SetData** doit être en mesure de reconnaître ces formats et de répondre de manière appropriée. Pour plus d’informations, consultez [gestion des scénarios de transfert de données de l’interpréteur](datascenarios.md)de commandes.

### <a name="enumformatetc-method"></a>Méthode EnumFormatEtc

Lorsque la cible reçoit un objet de données, il appelle généralement [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) pour déterminer les formats que l’objet contient. La méthode crée un objet d’énumération OLE et retourne un pointeur vers l’interface [**IEnumFORMATETC**](/windows/win32/api/objidl/nn-objidl-ienumformatetc) de l’objet. La cible utilise ensuite l’interface pour énumérer les formats disponibles.

Un objet d’énumération doit toujours énumérer les formats disponibles par ordre de qualité, en commençant par le meilleur. La qualité relative des formats est définie par la source de déplacement. En général, les formats de qualité supérieure contiennent les données les plus riches et les plus complètes. Par exemple, une image de couleur de 24 bits est normalement considérée comme une qualité supérieure à celle d’une version à échelle grise de cette image. La raison de l’énumération des formats dans l’ordre de leur qualité est que les cibles sont généralement énumérées jusqu’à ce qu’elles accèdent à un format pris en charge, puis utilisent ce format pour extraire les données. Pour que cette procédure produise le meilleur format disponible que la cible peut prendre en charge, les formats doivent être énumérés dans l’ordre de leur qualité.

Un objet d’énumération pour les données de l’interpréteur de commandes est implémenté à peu près de la même façon que pour d’autres types de transferts de données, avec une exception notable. Étant donné que les objets de données ne contiennent généralement qu’un seul élément de données par format, ils énumèrent normalement chaque format passé à [**IDataObject :: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata). Toutefois, comme indiqué dans la section [méthode SetData](#setdata-method) , les objets de données Shell peuvent contenir plusieurs formats [CFSTR \_ FILECONTENTS](clipboard.md) .

Étant donné que l’objectif de [**IDataObject :: EnumFormatEtc**](/windows/win32/api/objidl/nf-objidl-idataobject-enumformatetc) est de permettre à la cible de déterminer quels types de données sont présents, il n’est pas nécessaire d’énumérer plus d’un format [CFSTR \_ FILECONTENTS](clipboard.md) . Si la cible doit connaître le nombre de ces formats que contient l’objet de données, la cible peut récupérer ces informations à partir du \_ format CFSTR FILEDESCRIPTOR associé. Pour plus d’informations sur la façon d’implémenter **IDataObject :: EnumFormatEtc**, consultez la documentation de référence de la méthode.

### <a name="getdata-method"></a>GetData, méthode

La cible appelle [**IDataObject :: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) pour extraire un format de données particulier. La cible spécifie le format en passant la structure [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) appropriée. **IDataObject :: GetData** retourne la structure [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) du format.

La cible peut définir le membre **TYMED** de la structure [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) sur une valeur TYMED \_ *xxx* spécifique afin de spécifier le mécanisme de transfert de données qu’il utilisera pour extraire les données. Toutefois, la cible peut également effectuer une demande plus générique et laisser l’objet de données décider. Pour demander à l’objet de données de sélectionner le mécanisme de transfert de données, la cible définit toutes les valeurs TYMED \_ *xxx* qu’elle prend en charge. [**IDataObject :: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) sélectionne l’un de ces mécanismes de transfert de données et retourne la structure [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) appropriée. Par exemple, **TYMED** est généralement défini sur TYMED \_ HGLOBAL \| TYMED \_ ISTREAM \| TYMED \_ ISTORAGE pour demander l’un des trois mécanismes de transfert de données de Shell.

> [!Note]  
> Étant donné qu’il peut y avoir plusieurs formats [CFSTR \_ FILECONTENTS](clipboard.md) , les membres **cfFormat** et **TYMED** de la structure [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) ne sont pas suffisants pour indiquer la structure [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) que [**IDataObject :: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) doit retourner. Pour le \_ format CFSTR FILECONTENTS, **IDataObject :: GetData** doit également examiner le membre **Lindex** de la structure **FORMATETC** afin de retourner la structure **STGMEDIUM** correcte.

 

Le format [CFSTR \_ INDRAGLOOP](clipboard.md) est placé dans les objets de données pour permettre aux cibles de vérifier l’état de la boucle de glisser-déplacer tout en évitant le rendu gourmand en mémoire des données de l’objet. Les données du format sont une valeur **DWORD** qui est définie sur une valeur différente de zéro si l’objet de données se trouve dans une boucle de glissement. La valeur de données du format est définie sur zéro si les données ont été supprimées. Si une cible demande ce format et qu’elle n’a pas été chargée par la source, [**IDataObject :: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) doit répondre comme si la source avait chargé le format avec une valeur de zéro.

Lorsque le curseur se trouve sur la fenêtre cible, la cible peut utiliser l' [objet d’assistance glisser-déplacer](#using-the-drag-and-drop-helper-object) pour spécifier l’image de glissement. L’objet d’assistance par glisser-déplacer appelle [**IDataObject :: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) pour charger des formats privés dans l’objet de données utilisé pour la prise en charge inter-processus. Il appelle ensuite [**IDataObject :: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) pour les récupérer. Pour prendre en charge l’objet d’assistance par glisser-déplacer, votre implémentation d’objet de données Shell doit pouvoir retourner des formats privés arbitraires lorsqu’ils sont demandés.

### <a name="implementing-idropsource"></a>Implémentation de IDropSource

La source doit créer un objet qui expose une interface [**IDropSource**](/windows/win32/api/oleidl/nn-oleidl-idropsource) . Cette interface permet à la source de mettre à jour l' *image de glissement* qui indique la position actuelle du curseur et de fournir des commentaires au système sur la manière de mettre fin à une opération de glisser-déplacer. **IDropSource** a deux méthodes : [**GiveFeedback**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback) et [**QueryContinueDrag**](/windows/win32/api/oleidl/nf-oleidl-idropsource-querycontinuedrag).

### <a name="givefeedback-method"></a>GiveFeedback (méthode)

Pendant la boucle de glissement, une source de déplacement est chargée d’assurer le suivi de la position du curseur et d’afficher une image de glissement appropriée. Toutefois, dans certains cas, vous souhaiterez peut-être modifier l’apparence de l’image de glissement lorsqu’elle se trouve sur la fenêtre de la cible de déplacement.

Lorsque le curseur entre dans la fenêtre cible ou en sort, et Pendant qu’il se déplace au-dessus de la fenêtre cible, le système appelle régulièrement l’interface [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) de la cible. La cible répond avec une valeur [**DROPEFFECT**](../com/dropeffect-constants.md) qui est transférée à la source via la méthode [**GiveFeedback**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback) . Le cas échéant, la source peut modifier l’apparence du curseur en fonction de la valeur **DROPEFFECT** . Pour plus d’informations, consultez les références **GiveFeedback** et [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) .

### <a name="querycontinuedrag-method"></a>QueryContinueDrag (méthode)

Cette méthode est appelée si le bouton de la souris ou l’état du clavier change alors que l’objet de données se trouve dans la boucle de glissement. Elle indique à la source si la touche ÉCHAP a été enfoncée et fournit l’état actuel des touches de modification du clavier, telles que CTRL ou Maj. La valeur de retour de la méthode [**QueryContinueDrag**](/windows/win32/api/oleidl/nf-oleidl-idropsource-querycontinuedrag) spécifie l’une des trois actions suivantes :

-   \_OK. Continuer l’opération glisser
-   suppression d’DRAGDROP \_ S \_ . Supprimez les données. Le système appelle ensuite la méthode [**IDropTarget ::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) de la cible.
-   DRAGDROP \_ S \_ Annuler. Met fin à la boucle de glissement sans supprimer les données. Cette valeur est généralement retournée si la touche ÉCHAP a été enfoncée.

Pour plus d’informations, consultez les références [**QueryContinueDrag**](/windows/win32/api/oleidl/nf-oleidl-idropsource-querycontinuedrag) et [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) .

## <a name="how-a-target-handles-a-data-object"></a>Comment une cible gère un objet de données

La cible reçoit un objet de données lorsqu’il récupère l’objet de données du presse-papiers ou l’a supprimée de la fenêtre cible par l’utilisateur. La cible peut ensuite extraire des données de l’objet de données. Si nécessaire, la cible peut également notifier l’objet de données du résultat de l’opération. Avant un transfert de données Shell, une cible de déplacement doit se préparer pour l’opération :

1.  La cible doit appeler [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata) pour obtenir une valeur de format de presse-papiers valide pour tous les formats de Shell, à l’exception de [CF \_ HDROP](clipboard.md), qui peut être incluse dans l’objet de données. CF \_ HDROP est déjà un format de presse-papiers valide et n’a pas besoin d’être inscrit.
2.  Pour prendre en charge une opération de glisser-déplacer, la cible doit implémenter une interface [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) et inscrire une fenêtre cible. Pour inscrire une fenêtre cible, la cible appelle [**RegisterDragDrop**](/windows/win32/api/ole2/nf-ole2-registerdragdrop) et passe le handle de la fenêtre et le pointeur d’interface **IDropTarget** .

Pour les transferts du presse-papiers, la cible ne reçoit aucune notification indiquant qu’un objet de données a été placé dans le presse-papiers. En règle générale, une application est avertie qu’un objet se trouve dans le presse-papiers par une action de l’utilisateur, par exemple en cliquant sur le bouton coller dans la barre d’outils de l’application. La cible récupère ensuite le pointeur [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) de l’objet de données à partir du presse-papiers en appelant [**OleGetClipboard**](/windows/win32/api/ole2/nf-ole2-olegetclipboard). Pour les transferts de données par glisser-déplacer, le système utilise l’interface [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) de la cible pour fournir à la cible des informations sur la progression du transfert de données :

-   Le système appelle [**IDropTarget ::D ragenter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter) lorsque le curseur entre dans la fenêtre cible.
-   Le système appelle ensuite [**IDropTarget ::D ragover**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) lorsque le curseur passe sur la fenêtre cible, pour attribuer à la cible la position actuelle du curseur.
-   Le système appelle [**IDropTarget ::D ragleave**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragleave) lorsque le curseur quitte la fenêtre cible.
-   Le système appelle [**IDropTarget ::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) lorsque l’utilisateur dépose l’objet de données dans la fenêtre cible.

Pour plus d’informations sur l’implémentation de ces méthodes, consultez [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget).

Lorsque les données sont supprimées, [**IDropTarget ::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) fournit la cible avec un pointeur vers l’interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) de l’objet de données. La cible utilise ensuite cette interface pour extraire des données de l’objet de données.

### <a name="extracting-shell-data-from-a-data-object"></a>Extraction des données de l’interpréteur de commandes à partir d’un objet de données

Une fois qu’un objet de données a été supprimé ou récupéré du presse-papiers, la cible peut extraire les données dont il a besoin. La première étape du processus d’extraction consiste généralement à énumérer les formats contenus dans l’objet de données :

-   Appelez [**IDataObject :: EnumFormatEtc**](/windows/win32/api/objidl/nf-objidl-idataobject-enumformatetc). L’objet de données crée un objet énumération OLE standard et retourne un pointeur vers son interface [**IEnumFORMATETC**](/windows/win32/api/objidl/nn-objidl-ienumformatetc) .
-   Utilisez les méthodes [**IEnumFORMATETC**](/windows/win32/api/objidl/nn-objidl-ienumformatetc) pour énumérer les formats contenus dans l’objet de données. Cette opération récupère généralement une structure [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) pour chaque format que l’objet contient. Toutefois, l’objet d’énumération ne retourne normalement qu’une seule structure **FORMATETC** pour le format [CFSTR \_ FILECONTENTS](clipboard.md) , quel que soit le nombre de ces formats contenus dans l’objet de données.
-   Sélectionnez un ou plusieurs formats à extraire et stockez leurs structures [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) .

Pour récupérer un format particulier, transmettez la structure [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) associée à [**IDataObject :: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata). Cette méthode retourne une structure [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) qui fournit l’accès aux données. Pour spécifier un mécanisme de transfert de données particulier, définissez la valeur **TYMED** de la structure **FORMATETC** sur la \_ valeur TYMED *xxx* correspondante. Pour demander à l’objet de données de sélectionner un mécanisme de transfert de données, la cible définit les valeurs TYMED \_ *xxx* pour chaque mécanisme de transfert de données que la cible peut gérer. L’objet de données sélectionne l’un de ces mécanismes de transfert de données et retourne la structure **STGMEDIUM** appropriée.

Pour la plupart des formats, la cible peut récupérer les données en passant la structure [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) qu’elle a reçue lors de l’énumération des formats disponibles. Une exception à cette règle est [CFSTR \_ FILECONTENTS](clipboard.md). Comme un objet de données peut contenir plusieurs instances de ce format, la structure **FORMATETC** retournée par l’énumérateur peut ne pas correspondre au format particulier que vous souhaitez extraire. En plus de spécifier les membres **cfFormat** et **TYMED** , vous devez également définir le membre **Lindex** sur la valeur d’index du fichier. Pour plus d’informations, consultez la section *utilisation du \_ format CFSTR FILECONTENTS pour extraire des données à partir d’un fichier dans* gestion des scénarios de l' [interpréteur](datascenarios.md) de commandes transfert de données

Le processus d’extraction de données dépend du type de pointeur contenu dans la structure [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) retournée. Si la structure contient un pointeur vers une interface [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) ou [**IStorage**](/windows/win32/api/objidl/nn-objidl-istorage) , utilisez les méthodes d’interface pour extraire les données. Le processus d’extraction de données à partir d’un objet mémoire global est abordé dans la section suivante.

### <a name="extracting-a-global-memory-object-from-a-data-object"></a>Extraction d’un objet de mémoire globale à partir d’un objet de données

La plupart des formats de données de Shell se présentent sous la forme d’un objet de mémoire globale. Utilisez la procédure suivante pour extraire un format contenant un objet de mémoire globale à partir d’un objet de données et assigner ses données à une variable locale :

1.  Créer une structure [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) . Définissez le membre **cfFormat** sur la valeur de format du presse-papiers appropriée et le membre **TYMED** sur TYMED \_ HGLOBAL.
2.  Créez une structure [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) vide.
3.  Appelez [**IDataObject :: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata)et transmettez des pointeurs aux structures [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) et [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) .

    Quand [**IDataObject :: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) est retourné, la structure [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) contient un pointeur vers l’objet de mémoire globale qui contient les données.

4.  Assignez les données à une variable locale en appelant [**GlobalLock**](/windows/win32/api/winbase/nf-winbase-globallock) et en passant le membre **hGlobal** de la structure [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) .
5.  Appelez [**GlobalUnlock**](/windows/win32/api/winbase/nf-winbase-globalunlock) pour libérer le verrou sur l’objet de mémoire globale.
6.  Appelez [**ReleaseStgMedium**](/windows/win32/api/ole2/nf-ole2-releasestgmedium) pour libérer l’objet mémoire global.

> [!Note]  
> Vous devez utiliser [**ReleaseStgMedium**](/windows/win32/api/ole2/nf-ole2-releasestgmedium) pour libérer l’objet mémoire global, et non [**GlobalFree**](/windows/win32/api/winbase/nf-winbase-globalfree).

 

L’exemple suivant montre comment extraire une valeur **DWORD** stockée en tant qu’objet de mémoire globale à partir d’un objet de données. Le paramètre **pdtobj** est un pointeur vers l’interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) de l’objet de données, **CF** est le format de presse-papiers qui identifie les données souhaitées, et **pdwOut** est utilisé pour retourner la valeur de données.


```C++
STDAPI DataObj_GetDWORD(IDataObject *pdtobj, UINT cf, DWORD *pdwOut)
{    STGMEDIUM medium;
   FORMATETC fmte = {(CLIPFORMAT) cf, NULL, DVASPECT_CONTENT, -1, 
       TYMED_HGLOBAL};
    HRESULT hres = pdtobj->GetData(&fmte, &medium);
    if (SUCCEEDED(hres))
   {
       DWORD *pdw = (DWORD *)GlobalLock(medium.hGlobal);
       if (pdw)
       {
           *pdwOut = *pdw;
           GlobalUnlock(medium.hGlobal);
       }
       else
       {
           hres = E_UNEXPECTED;
       }
       ReleaseStgMedium(&medium);
   }
   return hres;
}
```



### <a name="implementing-idroptarget"></a>Implémentation de IDropTarget

Le système utilise l’interface [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) pour communiquer avec la cible lorsque le curseur se trouve sur la fenêtre cible. Les réponses de la cible sont transférées à la source via son interface [**IDropSource**](/windows/win32/api/oleidl/nn-oleidl-idropsource) . En fonction de la réponse, la source peut modifier l’icône qui représente les données. Si la cible de déplacement doit spécifier l’icône de données, elle peut le faire en créant un [objet d’assistance par glisser-déplacer](#using-the-drag-and-drop-helper-object).

Avec les opérations de glisser-déplacer conventionnelles, la cible informe l’objet de données du résultat de l’opération en définissant le paramètre *pdwEffect* de [**IDropTarget ::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) à la valeur [**DROPEFFECT**](../com/dropeffect-constants.md) appropriée. Avec les objets de données de l’interpréteur de commandes, la cible peut également avoir besoin d’appeler [**IDataObject :: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata). Pour plus d’informations sur la façon dont les cibles doivent répondre à différents scénarios de transfert de données, consultez [gestion des scénarios de transfert de données de l’interpréteur](datascenarios.md)de commandes.

Les sections suivantes décrivent brièvement comment implémenter les méthodes de l’exemple [**IDropTarget ::D ragenter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter), [**IDropTarget ::D ragover**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover)et [**IDropTarget ::D**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) . Pour plus d’informations, consultez la documentation de référence.

### <a name="dragenter-method"></a>DragEnter, méthode

Le système appelle la méthode [**IDropTarget ::D ragenter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter) lorsque le curseur entre dans la fenêtre cible. Ses paramètres fournissent la cible avec l’emplacement du curseur, l’état des touches de modification du clavier, telles que la touche CTRL, et un pointeur vers l’interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) de l’objet de données. La cible est chargée d’utiliser cette interface pour déterminer si elle peut accepter n’importe quel format contenu dans l’objet de données. Si tel est le cas, la valeur de *pdwEffect* reste inchangée. S’il ne peut pas accepter de données de l’objet de données, il définit le paramètre *pdwEffect* sur DROPEFFECT \_ None. Le système passe la valeur de ce paramètre à l’interface [**IDropSource**](/windows/win32/api/oleidl/nn-oleidl-idropsource) de l’objet de données pour lui permettre d’afficher l’image de glissement appropriée.

Les cibles ne doivent pas utiliser la méthode [**IDataObject :: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) pour restituer les données de l’interpréteur de commandes avant qu’elles aient été supprimées. Le rendu complet des données de l’objet pour chaque occurrence peut entraîner le blocage du curseur de glissement. Pour éviter ce problème, certains objets Shell contiennent un format [CFSTR \_ INDRAGLOOP](clipboard.md) . En extrayant ce format, les cibles peuvent vérifier l’état de la boucle de glissement tout en évitant le rendu gourmand en mémoire des données de l’objet. La valeur de données du format est une valeur **DWORD** qui est définie sur une valeur différente de zéro si l’objet de données se trouve dans une boucle de glissement. La valeur de données du format est définie sur zéro si les données ont été supprimées.

Si la cible peut accepter des données de l’objet de données, elle doit examiner **grfKeyState** pour déterminer si des touches de modification ont été enfoncées pour modifier le comportement de suppression normal. Par exemple, l’opération par défaut est généralement un déplacement, mais la pression sur la touche CTRL indique généralement une opération de copie.

Lorsque le curseur se trouve sur la fenêtre cible, la cible peut utiliser l' [objet d’assistance par glisser-déplacer](#using-the-drag-and-drop-helper-object) pour remplacer l’image de glissement de l’objet de données par son propre. Si c’est le cas, [**IDropTarget ::D ragenter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter) doit appeler [**IDropTargetHelper ::D ragenter**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragenter) pour passer les informations contenues dans les paramètres *DragEnter* à l’objet d’assistance de glisser-déplacer.

### <a name="dragover-method"></a>DragOver, méthode

Au fur et à mesure que le curseur se déplace dans la fenêtre cible, le système appelle périodiquement la méthode [**IDropTarget ::D ragover**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) . Ses paramètres fournissent la cible avec l’emplacement du curseur et l’état des touches de modification du clavier, telles que la touche CTRL. **IDropTarget ::D ragover** a les mêmes responsabilités que [**IDropTarget ::D ragenter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter), et les implémentations sont généralement très similaires.

Si la cible utilise l’objet d’assistance par glisser-déplacer, [**IDropTarget ::D ragover**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) doit appeler [**IDropTargetHelper ::D ragover**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragover) pour transférer les informations contenues dans les paramètres *DragOver* à l’objet d’assistance de glisser-déplacer.

### <a name="drop-method"></a>Drop, méthode

Le système appelle la méthode [**IDropTarget ::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) pour notifier à la cible que l’utilisateur a supprimé les données, en général en relâchant le bouton de la souris. **IDropTarget ::D ROP** a les mêmes paramètres que [**IDropTarget ::D ragenter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter). La cible répond normalement en extrayant un ou plusieurs formats de l’objet de données. Lorsque vous avez terminé, la cible doit définir le paramètre *pdwEffect* sur une valeur [**DROPEFFECT**](../com/dropeffect-constants.md) qui indique le résultat de l’opération. Pour certains types de transferts de données de Shell, la cible doit également appeler [**IDataObject :: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) pour passer un format avec des informations supplémentaires sur le résultat de l’opération à l’objet de données. Pour une présentation détaillée, consultez [gestion des scénarios de transfert de données de l’interpréteur](datascenarios.md)de commandes.

Si la cible utilise l’objet d’assistance par glisser-déplacer, [**IDropTarget ::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) doit appeler [**IDropTargetHelper ::D ROP**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-drop) pour transférer les informations contenues dans les paramètres [**IDropTargetHelper ::D ragover**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragover) à l’objet d’assistance de glisser-déplacer.

## <a name="using-the-drag-and-drop-helper-object"></a>Utilisation de l’objet d’assistance par glisser-déplacer

L’objet d’assistance par glisser-déplacer (CLSID \_ DragDropHelper) est exporté par l’interpréteur de commandes pour permettre aux cibles de spécifier l’image du glissement pendant qu’elle se trouve sur la fenêtre cible. Pour utiliser l’objet d’assistance par glisser-déplacer, créez un objet serveur in-process en appelant [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) avec un identificateur de classe (CLSID) de CLSID \_ DragDropHelper. L’objet d’assistance par glisser-déplacer expose deux interfaces qui sont utilisées de la façon suivante :

-   L’interface [**IDragSourceHelper**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idragsourcehelper) permet à la cible de déplacement de spécifier une icône pour représenter l’objet de données.
-   L’interface [**IDropTargetHelper**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idroptargethelper) permet à la cible de déplacement d’informer l’objet d’assistance du glisser-déplacer de l’emplacement du curseur, et d’afficher ou de masquer l’icône de données.

### <a name="using-the-idragsourcehelper-interface"></a>Utilisation de l’interface IDragSourceHelper

L’interface [**IDragSourceHelper**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idragsourcehelper) est exposée par l’objet d’assistance par glisser-déplacer pour permettre à une cible de déplacement de fournir l’image qui sera affichée lorsque le curseur se trouve sur la fenêtre cible. **IDragSourceHelper** fournit deux autres méthodes pour spécifier l’image bitmap à utiliser comme image de glissement :

-   Les cibles de dépôt qui ont une fenêtre peuvent enregistrer un \_ message de fenêtre di GETDRAGIMAGE pour celle-ci en initialisant l’objet d’assistance glisser-déplacer avec [**IDragSourceHelper :: InitializeFromWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idragsourcehelper-initializefromwindow). Lorsque la cible reçoit un \_ message di GETDRAGIMAGE, le gestionnaire place les informations de bitmap de l’image de glissement dans la structure [**SHDRAGIMAGE**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-shdragimage) qui est passée comme valeur *lParam* du message.
-   Les cibles de déplacement sans fenêtre spécifient une image bitmap lorsqu’elles initialisent l’objet d’assistance glisser-déplacer avec [**IDragSourceHelper :: InitializeFromBitmap**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idragsourcehelper-initializefrombitmap).

### <a name="using-the-idroptargethelper-interface"></a>Utilisation de l’interface IDropTargetHelper

Cette interface permet à la cible de déplacement de notifier l’objet d’assistance de glisser-déplacer lorsque le curseur entre dans la cible ou en sort. Lorsque le curseur se trouve sur la fenêtre cible, [**IDropTargetHelper**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idroptargethelper) permet à la cible de fournir à l’objet d’assistance glisser-déplacer les informations que la cible reçoit via son interface [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) .

Quatre des méthodes [**IDropTargetHelper**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idroptargethelper) ,[**IDropTargetHelper ::D ragenter**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragenter), [**IDropTargetHelper ::D Ragleave**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragleave), [**IDropTargetHelper ::D ragover**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragover)et [**IDropTargetHelper ::D ROP**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-drop), sont associées à la méthode [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) du même nom. Pour utiliser l’objet d’assistance par glisser-déplacer, chacune des méthodes **IDropTarget** doit appeler la méthode **IDropTargetHelper** correspondante pour transférer les informations à l’objet d’assistance de glisser-déplacer. La cinquième méthode **IDropTargetHelper** , [**IDropTargetHelper :: Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-show), notifie l’objet d’assistance glisser-déplacer pour afficher ou masquer l’image de glissement. Cette méthode est utilisée lors d’un glissement sur une fenêtre cible dans un mode vidéo de faible profondeur de couleur. Elle permet à la cible de masquer l’image glisser tout en peignant la fenêtre.

 

 
