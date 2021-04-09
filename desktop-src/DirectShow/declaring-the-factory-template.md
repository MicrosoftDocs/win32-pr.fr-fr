---
description: Déclaration du modèle de fabrique
ms.assetid: 3060c167-ea23-4061-b32a-16e750f55e6f
title: Déclaration du modèle de fabrique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3168f16b6281417846f13b7a17141282053c4705
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108630"
---
# <a name="declaring-the-factory-template"></a>Déclaration du modèle de fabrique

L’étape suivante consiste à déclarer le modèle de fabrique pour votre filtre. Un modèle de fabrique est une classe C++ qui contient des informations sur la fabrique de classe. Dans votre DLL, déclarez un tableau global d’objets [**CFactoryTemplate**](cfactorytemplate.md) , un pour chaque filtre ou composant COM dans votre dll. Le tableau doit être nommé *\_ modèles g*. Pour plus d’informations sur les modèles de fabrique, voir [How to Create a DirectShow Filter dll](how-to-create-a-dll.md).

Le membre de **\_ \_ filtre m pAMovieSetup** du modèle de fabrique est un pointeur vers la structure de [**\_ filtre AMOVIESETUP**](amoviesetup-filter.md) décrite précédemment. L’exemple suivant montre un modèle de fabrique, à l’aide de la structure donnée dans l’exemple précédent :


```C++
CFactoryTemplate g_Templates[] = {
    {
        g_wszName,                      // Name.
        &CLSID_SomeFilter,              // CLSID.
        CSomeFilter::CreateInstance,    // Creation function.
        NULL,
        &sudFilterReg                   // Pointer to filter information.
    }
};
int g_cTemplates = sizeof(g_Templates) / sizeof(g_Templates[0]);
```



Si vous n’avez pas déclaré d’informations de filtre, **m \_ pAMoveSetup \_ Filter** peut avoir la **valeur null**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Comment inscrire des filtres DirectShow](how-to-register-directshow-filters.md)
</dt> </dl>

 

 



