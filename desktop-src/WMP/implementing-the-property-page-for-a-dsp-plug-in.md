---
title: Implémentation de la page de propriétés pour un plug-in DSP
description: Implémentation de la page de propriétés pour un plug-in DSP
ms.assetid: 3dd3e547-fd06-4f01-8731-da1f8c958a32
keywords:
- Plug-ins du lecteur Windows Media, DSP audio
- plug-ins, DSP audio
- plug-ins de traitement de signal numérique, propriétés audio
- Plug-ins DSP, propriétés audio
- plug-ins DSP audio, propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aec87318b77fec4e9218398c1cb43dd5954a49e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839682"
---
# <a name="implementing-the-property-page-for-a-dsp-plug-in"></a>Implémentation de la page de propriétés pour un plug-in DSP

Le lecteur Windows Media peut afficher une page de propriétés pour chaque plug-in DSP afin de permettre aux utilisateurs de définir des valeurs qui modifient le comportement du plug-in. Les utilisateurs peuvent accéder à la page de propriétés à partir de l’onglet **plug-ins** de la boîte de dialogue Options en cliquant sur le nom du plug-in DSP pour le sélectionner, puis en cliquant sur **Propriétés**.

L’exemple de code du plug-in du lecteur Windows Media fournit une implémentation par défaut d’une page de propriétés qui inclut une seule zone d’édition qui reçoit de l’utilisateur une valeur représentant un facteur d’échelle pour le volume audio. Quand l’utilisateur clique sur **appliquer**, la page de propriétés transmet cette valeur à l’objet de plug-in afin que le plug-in puisse modifier la valeur qu’il utilise pour mettre à l’échelle le volume au cours du traitement.

## <a name="about-the-property-page-object"></a>À propos de l’objet page de propriétés

L’objet page de propriétés est un objet COM qui implémente l’interface **IPropertyPage** . L’exemple de code généré par l’Assistant de plug-in utilise l’implémentation ATL de **IPropertyPage**, qui est documentée dans la documentation Visual C++ sur MSDN. Votre code doit au moins fournir des implémentations de substitution pour **IPropertyPage :: OnInitDialog**, qui gère l’événement qui se produit lorsque la page de propriétés s’ouvre, et **IPropertyPage :: apply**, qui gère l’événement qui se produit lorsque l’utilisateur clique sur **appliquer**. L’Assistant de plug-in génère un exemple de code pour chacun de ces gestionnaires d’événements. L’exemple d’implémentation de **OnInitDialog** récupère une valeur du Registre afin de pouvoir afficher le paramètre de facteur d’échelle actuel. L’exemple d’implémentation de **apply** valide l’entrée utilisateur en test pour s’assurer qu’il se trouve dans une plage spécifiée, puis conserve la valeur dans le registre, puis passe la valeur (si valide) à la méthode put de la propriété du plug-in DSP, nommée **put \_ Scale**.

En outre, vous devrez ajouter du code pour gérer l’événement qui se produit lorsque l’utilisateur modifie une valeur dans un contrôle que vous fournissez dans la page de propriétés. Par exemple, l’Assistant de plug-in implémente une fonction nommée **OnChangeScale**, qui active simplement le bouton **appliquer** lorsque l’utilisateur modifie le texte de la zone d’édition sur la page de propriétés en appelant la méthode **SetDirty** avec la valeur d’argument **true**.

## <a name="about-the-property-page-dialog-resource"></a>À propos de la ressource de boîte de dialogue page de propriétés

L’interface utilisateur de la page de propriétés est stockée sous la forme d’une ressource de boîte de dialogue. Vous pouvez facilement afficher et modifier la boîte de dialogue de la page de propriétés dans Visual Studio en sélectionnant l’onglet **ResourceView** dans la fenêtre espace de travail du projet, puis en ouvrant le dossier de la **boîte de dialogue** , puis en double-cliquant sur le nom de ressource de la page de propriétés. L’éditeur de ressources de boîtes de dialogue dans Visual Studio vous fournit les outils dont vous avez besoin pour ajouter des contrôles à la boîte de dialogue de la page de propriétés et créer des gestionnaires d’événements qui sont mappés aux messages Windows appropriés. Pour plus d’informations sur l’utilisation de l’éditeur de ressources dans Visual Studio, reportez-vous à l’aide de Visual Studio.

## <a name="about-ispecifypropertypages"></a>À propos de ISpecifyPropertyPages

Si un plug-in DSP fournit une page de propriétés, le plug-in doit implémenter l’interface **ISpecifyPropertyPages** . Cette interface contient une seule méthode : **ISpecifyPropertyPages :: GetPages**. Il s’agit de la méthode qui associe la page de propriétés au plug-in DSP. Le lecteur Windows Media appelle cette méthode lorsque l’utilisateur appelle la page de propriétés, en passant un paramètre de type cauuid, qui est un tableau compté de GUID. L’exemple d’implémentation de plug-in de **GetPages** remplit cette structure avec un GUID unique qui est l’ID de classe de l’objet de la page de propriétés du plug-in. Le lecteur Windows Media utilise alors l’ID de classe pour créer l’objet de page de propriétés.

Vous pouvez remarquer que l’exemple d’implémentation de **GetPages** utilise **CoTaskMemAlloc** pour allouer de la mémoire pour la structure GUID. Il incombe à l’appelant, dans ce cas Windows Media Player, d’utiliser **CoTaskMemFree** pour libérer de la mémoire. Pour plus d’informations sur la structure cauuid, consultez la documentation du kit de développement Platform SDK.

## <a name="about-the-proxystub-dll"></a>À propos de la DLL proxy/stub

Pour qu’un plug-in DSP fonctionne dans le lecteur Windows Media 11 s’exécutant sur Windows Vista, vous devez fournir une DLL proxy/stub pour les interfaces personnalisées utilisées pour communiquer les modifications apportées aux paramètres d’une boîte de dialogue de page de propriétés à la classe de plug-in. Les appels de méthode effectués via ces interfaces doivent être marshalés lorsque les appels sont effectués sur des limites de processus ou de cloisonnement. La dernière version de l’Assistant de plug-in crée un exemple de projet de DLL de proxy/stub.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Implémentation d’un plug-in DSP audio**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




