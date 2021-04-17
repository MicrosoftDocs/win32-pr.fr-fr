---
description: Un plug-in de rendu dynamique est un objet qui affiche les données du stylet en temps réel, car il est géré par l’objet RealTimeStylus.
ms.assetid: ac6d15f3-0917-4cc1-8c83-e34d3d063289
title: Plug-ins Dynamic-Renderer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c3f1a33c3cd7faef2e899bcb198ea64aa5bd76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104567766"
---
# <a name="dynamic-renderer-plug-ins"></a>Plug-ins Dynamic-Renderer

Un plug-in de rendu dynamique est un objet qui affiche les données du stylet en temps réel, car il est géré par l’objet [**RealTimeStylus**](realtimestylus-class.md) . Plus tard, pour les événements tels que l’actualisation d’un formulaire, le plug-in de rendu dynamique ou un plug-in de collecteur d’encre peut redessiner l’encre.

## <a name="the-dynamicrenderer-object"></a>Objet DynamicRenderer

L’objet [**RealTimeStylus**](realtimestylus-class.md) implémente l’interface [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) . L’objet [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) restitue l’encre en temps réel, lors de son dessin. Quand la méthode [**Refresh**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-refresh) est appelée alors que l’objet **DynamicRenderer** est activé, l’objet **DynamicRenderer** redessine le trait en cours de collecte. La propriété [**Enabled**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-get_enabled) de l’objet **DynamicRenderer** est initialement définie sur **false**.

> [!Note]  
> Lors de l’appel de la méthode [**Refresh**](/previous-versions/ms826370(v=msdn.10)) de l’objet [**DynamicRenderer**](/previous-versions/ms826345(v=msdn.10)) à partir d’un gestionnaire d’événements [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) dans du code managé, définissez la propriété [**ClipRectangle**](/previous-versions/ms826346(v=msdn.10)) de l’objet **DynamicRenderer** sur la propriété [ClipRectangle](/dotnet/api/system.windows.forms.painteventargs.cliprectangle?view=netcore-3.1) de l’objet [PaintEventArgs](/dotnet/api/system.windows.forms.painteventargs?view=netcore-3.1) .

 

L’objet [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) peut mettre temporairement en cache les données d’encre. Pour utiliser cette fonctionnalité dans du code managé, affectez à la propriété [EnableDataCache](/previous-versions/ms826349(v=msdn.10)) la **valeur true**. Lorsque l’objet [**DynamicRenderer**](/previous-versions/ms826345(v=msdn.10)) reçoit un appel à sa méthode [**IStylusSyncPlugin. StylusUp**](/previous-versions/ms826366(v=msdn.10)) , il met en cache les données de trait et ajoute des données de stylet personnalisées à la file d’attente d’entrée en réponse à l’objet [**StylusUpData**](/previous-versions/ms824057(v=msdn.10)) pour le trait. La propriété [CustomDataId](/previous-versions/ms824749(v=msdn.10)) de l’objet [**CustomStylusData**](/previous-versions/ms824747(v=msdn.10)) est définie sur la valeur [DynamicRendererCachedDataGuid](/previous-versions/ms824744(v=msdn.10)) et la propriété Data de l’objet **CustomStylusData** contient un objet DynamicRendererCachedData. Appelez la méthode [ReleaseCachedData](/previous-versions/ms826371(v=msdn.10)) de l’objet **DynamicRenderer** une fois que le trait a été collecté et peut être rendu statiquement. Quand la méthode [**Refresh**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-refresh) est appelée alors que l’objet **DynamicRenderer** est activé, l’objet **DynamicRenderer** redessine tous les traits mis en cache. Lorsque la propriété [**DataCacheEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-get_datacacheenabled) est définie sur **false**, les données de trait mises en cache sont supprimées.

Le diagramme suivant illustre la façon dont l’objet [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) ajoute des données aux données du stylet de tablette lorsque la propriété [**DataCacheEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-get_datacacheenabled) de l’objet **DynamicRenderer** est définie.

![Illustration montrant le circuit de données DynamicRenderer](images/75f4ee7b-160c-410e-bfae-dfc676a9829c.gif)

Dans ce diagramme, le cercle « SD » représente un objet [**StylusDown**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusdown) et les cercles « P » représentent les objets de [**paquets**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-packets) qui ont déjà été ajoutés à la file d’attente de sortie de l’objet [**RealTimeStylus**](realtimestylus-class.md) et qui n’ont pas encore été envoyés à la collection de plug-ins asynchrone. Le cercle « SU » est représenté par un objet [**StylusUp**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusup) que l’objet **RealTimeStylus** est en train de traiter. Il est envoyé à la collection de plug-ins synchrone, puis placé dans la file d’attente de sortie. Les cercles « récupération d’urgence » représentent les données personnalisées du stylet qui sont ajoutées à la file d’attente d’entrée par le plug-in [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) en réponse à la notification du stylet associée à « su ». Les données de stylet personnalisées « récupération d’urgence » sont ensuite transmises aux plug-ins synchrones, puis à la file d’attente de sortie avant le traitement des données du stylet de tablette suivant. Le cercle vide représente la position dans la file d’attente de sortie où les futures données de stylet du Tablet PC sont ajoutées. Également représenté sur le diagramme, il s’agit du plug-in Ink-Collector appelant la méthode [**ReleaseCachedData**](/windows/desktop/api/RTSCom/nf-rtscom-idynamicrenderer-releasecacheddata) de l’objet **DynamicRenderer** pour libérer les données du trait mis en cache une fois que le plug-in de la collection d’encres a traité le trait.

### <a name="special-considerations"></a>Considérations spéciales

La liste suivante décrit d’autres points à prendre en compte lors de l’utilisation de l’objet [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) .

-   Vous ne devez pas attacher un objet [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) à plusieurs objets [**RealTimeStylus**](realtimestylus-class.md) . Une fois que deux objets **RealTimeStylus** auxquels l’objet **DynamicRenderer** est attaché sont activés, les éléments suivants se produisent.

    -   L’objet [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) lève une exception en réponse au deuxième appel à sa méthode [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) .
    -   Le deuxième objet [**RealTimeStylus**](realtimestylus-class.md) qui a été activé génère un objet d' [**erreur**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) et notifie les autres plug-ins dans ses collections de plug-ins de l’erreur.
    -   L’objet [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) arrête le rendu des données du stylet de tablette.

-   L’objet [**RealTimeStylus**](realtimestylus-class.md) lève une exception lorsque sa méthode [**AddCustomStylusDataToQueue**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-addcustomstylusdatatoqueue) est appelée avec le paramètre *GUID* défini sur l’identificateur global unique (Guid) DynamicRendererCachedDataGuid.
-   L’objet [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) est implémenté en tant que wrapper COM (Component Object Model) et vous ne pouvez pas appeler directement ses méthodes d’interface [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) . Pour plus d’informations sur l’opération COM et l’objet [**RealTimeStylus**](realtimestylus-class.md) , consultez [Remarques d’implémentation pour les API StylusInput](implementation-notes-for-the-stylusinput-apis.md).

## <a name="custom-rendering"></a>Rendu personnalisé

Vous pouvez créer votre propre plug-in de rendu dynamique en créant un plug-in synchrone qui s’abonne aux notifications [**StylusDown**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusdown), [**paquets**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-packets)et [**StylusUp**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusup) . Votre plug-in peut ensuite afficher le trait au fur et à mesure qu’il est dessiné. Il peut s’agir d’une façon d’implémenter un outil de sélection qui utilise une zone de sélection ou de sélection de forme libre, par exemple.

 

 
