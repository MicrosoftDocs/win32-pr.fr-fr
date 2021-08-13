---
title: dual (attribut)
description: L’attribut double identifie une interface qui expose des propriétés et des méthodes par le biais de IDispatch et directement par le biais du VTBL.
ms.assetid: 1c214f10-57eb-4a05-99a8-a09770666a74
keywords:
- MIDL avec deux attributs
topic_type:
- apiref
api_name:
- dual
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1e1e9cd15c1b219d07518c9630880a5010226c96c63d57539ffb66fab3a6c02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118643093"
---
# <a name="dual-attribute"></a>dual (attribut)

L’attribut **double** identifie une interface qui expose des propriétés et des méthodes par le biais de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) et directement par le biais du VTBL.

``` syntax
[
    uuid(uuid-number), 
    oleautomation,
    dual 
  [ , optional-attribute-list]
]
interface interface-name
{
    . . .
};
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*UUID-Number* 
</dt> <dd>

Spécifie un numéro d’identification unique universel pour l’interface

</dd> <dt>

*Optional-attribute-List* 
</dt> <dd>

Spécifie une liste de zéro ou plusieurs attributs MIDL supplémentaires.

</dd> <dt>

*nom de l’interface* 
</dt> <dd>

Nom de l’interface à laquelle l’attribut **double** sera appliqué.

</dd> </dl>

## <a name="remarks"></a>Remarques

Les interfaces identifiées par l’attribut **double** doivent être compatibles avec l’automatisation et être dérivées de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch). Cet attribut n’est pas autorisé sur les dispinterfaces.

L’attribut **double** crée une interface qui est à la fois une interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) et une interface com (Component Object Model). Les sept premières entrées du VTBL pour une interface double sont les sept membres de **IDispatch**, et les entrées restantes sont destinées à un accès direct aux membres de l’interface double. Tous les paramètres et types de retour spécifiés pour les membres d’une interface double doivent être des types compatibles Automation.

Tous les membres d’une interface double doivent passer un HRESULT comme valeur de retour de la fonction. Les membres, tels que les fonctions d’accesseur de propriété, qui doivent retourner d’autres valeurs, doivent spécifier le dernier paramètre comme [**out**](out-idl.md), [**retVal**](retval.md), indiquant un paramètre de sortie qui retourne la valeur de la fonction. En outre, les membres qui doivent prendre en charge plusieurs paramètres régionaux doivent passer un paramètre [**LCID**](lcid.md) .

Une interface double fournit à la fois la vitesse de liaison VTBL directe et la flexibilité de la liaison [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . Pour cette raison, les interfaces doubles sont recommandées dans la mesure du possible.

> [!Note]  
> Si votre application accède à des données d’objet en effectuant un cast du pointeur *This* dans l’appel d’interface, vous devez vérifier les pointeurs VTBL dans l’objet par rapport à vos propres pointeurs VTBL pour vous assurer que vous êtes connecté au proxy approprié.

 

Si vous spécifiez **double** sur une interface, cela signifie que l’interface est compatible avec Automation et, par conséquent, les \_ indicateurs TYPEFLAG FDUAL et TYPEFLAG \_ FOLEAUTOMATION sont définis.

### <a name="flags"></a>Indicateurs

TYPEFLAG \_ FDUAL, TYPEFLAG \_ FOLEAUTOMATION

## <a name="examples"></a>Exemples

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    oleautomation, dual
]
interface IHello : IDispatch
{
    //Diverse properties and methods defined here.
};
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Génération d’une bibliothèque de types avec MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**interface**](interface.md)
</dt> <dt>

[**LCID**](lcid.md)
</dt> <dt>

[**oleautomation**](oleautomation.md)
</dt> <dt>

[Syntaxe du fichier ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemple de fichier ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[**à**](out-idl.md)
</dt> <dt>

[**retval**](retval.md)
</dt> </dl>

 

 