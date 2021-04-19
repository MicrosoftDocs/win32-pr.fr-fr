---
description: Fournit un modèle pour créer des fabriques de classes.
ms.assetid: 3dbe6402-15f8-4490-9fe2-bebaa4e79170
title: CFactoryTemplate, classe (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFactoryTemplate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: be5ca9b8319eeddf777cbf0071c1930f21524369
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537990"
---
# <a name="cfactorytemplate-class"></a>CFactoryTemplate, classe

Fournit un modèle pour créer des fabriques de classes.

Dans DirectShow, les fabriques de classes sont spécialisées à l’aide de la classe **CFactoryTemplate** , également appelée *modèle de fabrique*. Chaque fabrique de classe contient un pointeur vers un modèle de fabrique. Le modèle de fabrique contient des informations sur un objet COM, y compris l’identificateur de classe (CLSID) de l’objet et un pointeur vers une fonction qui crée l’objet.

Dans votre DLL, déclarez un tableau global de modèles de fabrique nommés *g \_ Templates*. Incluez un modèle de fabrique pour chaque objet dans la DLL. Quand la fonction [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) crée une nouvelle fabrique de classes, elle recherche un modèle avec un CLSID correspondant dans le tableau. En supposant qu’il en trouve un, il crée une fabrique de classe qui contient un pointeur vers le modèle correspondant. Lorsque le client appelle **IClassFactory :: CreateInstance**, la fabrique de classe appelle la fonction d’instanciation définie dans le modèle.

Pour plus d’informations, voir [How to Create a DirectShow Filter dll](how-to-create-a-dll.md).



| Variables membres publiques                                                   | Description                                                                |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [**\_nom m**](cfactorytemplate-m-name.md)                                | Nom du filtre.                                                        |
| [**m \_ ClsID**](cfactorytemplate-m-clsid.md)                              | Pointeur vers le CLSID de l’objet.                                        |
| [**m \_ lpfnNew**](cfactorytemplate-m-lpfnnew.md)                          | Pointeur vers une fonction qui crée une instance de l’objet.              |
| [**m \_ lpfnInit**](cfactorytemplate-m-lpfninit.md)                        | Pointeur vers une fonction qui est appelée à partir du point d’entrée de la DLL.           |
| [**\_filtre m pAMovieSetup \_**](cfactorytemplate-m-pamoviesetup-filter.md) | Pointeur vers une structure de [**\_ filtre AMOVIESETUP**](amoviesetup-filter.md) . |
| M&#233;thodes publiques                                                            | Description                                                                |
| [**IsClassID**](cfactorytemplate-isclassid.md)                           | Détermine si un CLSID correspond à ce modèle de classe.                    |
| [**CreateInstance**](cfactorytemplate-createinstance.md)                 | Appelle la fonction de création d’objet pour la classe.                          |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>ComBase. h (include streams. h)</dt> </dl>                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib ; </dt> <dt>Strmbasd. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Référence de classe de base](base-class-reference.md)
</dt> </dl>

 

