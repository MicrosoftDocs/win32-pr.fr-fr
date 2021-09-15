---
description: En savoir plus sur les mots clés configurables par l’utilisateur dans le schéma d’impression pour la gestion des couleurs, telles que PageColorManagement et PageBlackGenerationProcessing.
ms.assetid: 296255b8-fe5c-46dd-b717-487aaae0db80
title: Gestion des couleurs et schéma d’impression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9258d9dcc59ab24f9cfca8e170bf3f3f62841b21
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412831"
---
# <a name="color-management-and-the-print-schema"></a>Gestion des couleurs et schéma d’impression

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Les mots clés d’éléments configurables par l’utilisateur peuvent être spécifiques au XPS ou non à XPS. Dans le cas où elles ne sont pas spécifiques à XPS, le mot clé peut être utilisé pour l’impression héritée basée sur GDI. Si une application décide de définir ces mots clés dans un PrintTicket, il revient au pilote de déterminer l’action et le comportement appropriés à prendre en fonction des définitions présentées dans le schéma d’impression. L’un de ces mots clés peut être utilisé dans le contexte de ICM. pour plus d’informations, consultez le kit de développement logiciel (SDK) Windows Vista.



| Schéma d’impression-mot clé configurable utilisateur       | Équivalent DEVMODE     | Spécifique à XPS   |
|----------------------------------------------|------------------------|----------------|
| PageColorManagement<br/>               | dmICMMethod<br/> | Non<br/>  |
| PageBlackGenerationProcessing<br/>     | None<br/>        | Oui<br/> |
| PageBlendColorSpace<br/>               | None<br/>        | Oui<br/> |
| PageSourceColorProfile<br/>            | Aucun<br/>        | Non<br/>  |
| PageDestinationColorProfile<br/>       | Aucun<br/>        | Non<br/>  |
| PageICMRenderingIntent<br/>            | dmICMIntent<br/> | Non<br/>  |
| JobOptimalDestinationColorProfile<br/> | Aucun<br/>        | Non<br/>  |
| PageDeviceColorSpaceUsage<br/>         | None<br/>        | Oui<br/> |



 

## <a name="pagecolormanagement-system-handling"></a>Gestion du système PageColorManagement

Pour PageColorManagement, le système assure la gestion automatique de PrintTicket à DEVMODE ou DEVMODE à la conversion PrintTicket, si nécessaire. Cela dépend du chemin d’impression spécifique entre l’application (Win32 ou WPF) et le pilote (GDI ou XPSDrv). dans le cas d’une impression à partir d’une application Windows Presentation Foundation sur un pilote d’impression Microsoft XPSDrv, une option publique PageColorManagement du système ne doit pas être publiée dans le document PrintTicket ou PrintCapabilities. dans ce cas, la gestion des couleurs ne peut pas être gérée automatiquement par le système. L’impression à partir d’une application Win32 sur un pilote d’impression Microsoft XPSDrv peut entraîner la gestion des couleurs entre l’application et GDI, toutefois, après la conversion au format XPS, il n’y aura pas de traitement automatique du système de gestion des couleurs entre le document XPS et le pilote et/ou le périphérique, car le format XPS-met en forme chaque élément avec des informations de couleur complètes, et il appartient au pilote ou à l’appareil de traiter ces informations.



| Options publiques PageColorManagement | Valeur DEVMODE                  |
|------------------------------------|--------------------------------|
| None<br/>                    | DMICMMETHOD \_ aucun<br/>   |
| Périphérique<br/>                  | \_appareil DMICMMETHOD<br/> |
| Pilote<br/>                  | \_pilote DMICMMETHOD<br/> |
| Système<br/>                  | \_système DMICMMETHOD<br/> |



 

## <a name="pageicmrenderingintent-system-handling"></a>Gestion du système PageICMRenderingIntent

Pour PageICMRenderingIntent, le système assure la gestion automatique de PrintTicket à DEVMODE ou DEVMODE à la conversion PrintTicket, si nécessaire. cela dépend du chemin d’impression spécifique entre l’application (Win32 ou Windows Presentation Foundation) et le pilote (GDI ou XPSDrv).



| Options publiques PageICMRenderingIntent | Valeur DEVMODE                       |
|---------------------------------------|-------------------------------------|
| AbsoluteColorimetric<br/>       | \_COLORIMÉTRIE DMICM ABS \_<br/> |
| RelativeColorimetric<br/>       | \_COLORIMÉTRIE DMICM<br/>      |
| Photos<br/>                | \_contraste DMICM<br/>          |
| BusinessGraphics<br/>           | \_saturation DMICM<br/>          |



 

Tous les autres mots clés liés à la gestion des couleurs (autres que PageColorManagement ou PageICMRenderingIntent) ne disposent pas de ce type de gestion automatique.

## <a name="joboptimaldestinationcolorprofile-and-pagedestinationcolorprofile-usage"></a>Utilisation de JobOptimalDestinationColorProfile et de PageDestinationColorProfile

Une application peut décider d’interroger le document PrintCapabilities pour JobOptimalDestinationColorProfile. Cela peut permettre à une application d’obtenir le profil de couleurs optimal en fonction de la configuration actuelle de l’appareil, tel que défini dans le document PrintCapabilities. Si l’application décide qu’elle souhaiterait que le pilote effectue la gestion des couleurs sur le profil de couleurs de destination spécifié par JobOptimalDestinationColorProfile, PageColorManagement et PageDestinationColorProfile sont respectivement définis sur Driver et DriverConfiguration dans PrintTicket. Si l’application ne souhaite pas utiliser le JobOptionalDestinationColorProfile et choisit d’utiliser sa propre valeur, elle doit définir PageColorManagement sur None et définir PageDestinationColorProfile sur application dans PrintTicket pour indiquer que l’application a déjà effectué la gestion des couleurs à son profil de couleurs de destination spécifié. Un autre scénario peut se produire lorsque l’application choisit d’utiliser le profil de couleur de destination optimal renvoyé par les pilotes PrintCapabilities, mais décide de procéder à la gestion des couleurs. Dans ce cas, PageColorManagement est défini sur None et PageDestinationColorProfile est défini sur application.

## <a name="pagesourcecolorprofile-usage"></a>Utilisation de PageSourceColorProfile

Pour PageSourceColorProfile, une application peut spécifier un profil de couleurs source pour chaque page dans le PrintTicket, quelle que soit l’option sélectionnée pour PageColorManagement. Qu’il soit présent ou non, il revient au pilote de déterminer le comportement de chaque cas en fonction des définitions présentées dans le schéma d’impression. Par exemple, une application peut affecter la valeur None à PageColorManagement, puis ne pas définir PageSourceColorProfile dans PrintTicket. Il est également possible pour une application de définir PageColorManagement sur Driver, puis de définir PageSourceColorProfile dans PrintTicket. dans ce cas, le pilote est chargé de déterminer le comportement dans les instructions du PrintSchema.

## <a name="pagedevicecolorspaceusage"></a>PageDeviceColorSpaceUsage

PageDeviceColorSpaceUsage est un élément configurable par l’utilisateur spécifique à XPS défini par l’application. Il fournit des instructions pour l’appareil en définissant l’option appropriée dans PrintTicket, pour la gestion des profils d’espace colorimétrique associés dans un document XPS. L’application et/ou le PrintTicket existant peut spécifier ce mot clé dans un PrintTicket envoyé à l’appareil. Qu’il soit présent ou non, il revient au pilote de déterminer le comportement de chaque cas, en fonction des définitions présentées dans le schéma d’impression.

## <a name="print-schema-color-management-example-flow"></a>Exemple de gestion des couleurs du schéma d’impression Flow

Le diagramme suivant illustre le déroulement des scénarios les plus probables pour l’utilisation de la gestion des couleurs et du schéma d’impression. Pour des raisons de simplicité et de lisibilité, seuls les mots clés de schéma d’impression configurables suivants ont été utilisés pour illustrer leur utilisation : PageColorManagement, JobOptimalDestinaionColorProfile, PageSourceColorProfile et PageDestinationColorProfile. Une ligne pleine représente une action qui doit se produire et une ligne en pointillés représente une action qui peut se produire. Le scénario suivant n’est pas l’interaction garantie qui se traduira par l’application, le pilote et le système. Toutefois, il représente le cas d’utilisation le plus courant.

![diagramme qui montre comment les paramètres de gestion des couleurs sont traités](images/local-1992284846-colormanagementtest3.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




