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
ms.openlocfilehash: 1f9fbc76fe65e1f1136fb44d22db36500c4d8870f97befa8e36fa08a108ada71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697619"
---
# <a name="cfactorytemplate-class"></a>CFactoryTemplate, classe

Fournit un modèle pour créer des fabriques de classes.

dans DirectShow, les fabriques de classes sont spécialisées à l’aide de la classe **CFactoryTemplate** , également appelée *modèle de fabrique*. Chaque fabrique de classe contient un pointeur vers un modèle de fabrique. Le modèle de fabrique contient des informations sur un objet COM, y compris l’identificateur de classe (CLSID) de l’objet et un pointeur vers une fonction qui crée l’objet.

Dans votre DLL, déclarez un tableau global de modèles de fabrique nommés *g \_ Templates*. Incluez un modèle de fabrique pour chaque objet dans la DLL. Quand la fonction [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) crée une nouvelle fabrique de classes, elle recherche un modèle avec un CLSID correspondant dans le tableau. En supposant qu’il en trouve un, il crée une fabrique de classe qui contient un pointeur vers le modèle correspondant. Lorsque le client appelle **IClassFactory :: CreateInstance**, la fabrique de classe appelle la fonction d’instanciation définie dans le modèle.

pour plus d’informations, voir [How to create a DirectShow Filter DLL](how-to-create-a-dll.md).



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
| En-tête<br/>  | <dl> <dt>combase. h (inclure Flux. h)</dt> </dl>                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib ; </dt> <dt>Strmbasd. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Référence de classe de base](base-class-reference.md)
</dt> </dl>

 

