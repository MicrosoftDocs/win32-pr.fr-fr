---
title: URI dans Windows 8.1
description: Windows 8.1 autorise uniquement les URI https, pas les URI http
ms.assetid: 06BDD3A3-67B7-4085-83DA-F322F718C876
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 994780798bfe7ada0d7dc49794deb284e30f1605
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382544"
---
# <a name="windows-81-allows-only-https-uris-not-http-uris"></a>Windows 8.1 autorise uniquement les URI https, pas les URI http

## <a name="platforms"></a>Plateformes

<dl> Clients-Windows 8.1  
Serveurs-Windows Server 2012 R2  
</dl>

## <a name="description"></a>Description

Alors que les applications générées pour Windows 8 peuvent inclure des URI http et https dans leurs URI de contenu d’application, les applications générées pour Windows 8.1 peuvent inclure uniquement des URI HTTPS.

La seule exception concerne les ContentUriRules dynamiques spécifiés dans le fichier AppxManifest.xml de l’application. Avec les ContentUriRules dynamiques, les applications peuvent accéder à des domaines supplémentaires ou à des ressources réseau fournies par l’administrateur, par exemple des URI stratégie de groupe. Toutefois, les ContentUriRules dynamiques sont uniquement disponibles pour les applications du Windows Store si elles remplissent les conditions suivantes :

-   Le stratégie de groupe est activé
-   Le package a spécifié la fonctionnalité enterpriseAuthentication
-   Le OSMaxVersionTested du package est Windows 8.1 ou supérieur

Les nouvelles restrictions dans Windows 8.1 font partie des restrictions de sécurité renforcée pour renforcer la protection de la plateforme.

## <a name="manifestations"></a>Manifestations

Lors de l’exécution d’une application conçue pour Windows 8 sur Windows 8.1, l’utilisation d’URI http dans le [ApplicationContentUriRules](/uwp/schemas/appxpackage/appxmanifestschema/element-applicationcontenturirules) est autorisée.

## <a name="mitigations"></a>Corrections

Nous recommandons que les développeurs WWA basculent de [<iframe>](https://msdn.microsoft.com/library/windows/apps/hh465955.aspx) vers le contrôle [WebView](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) (<x-ms-WebView>). Toutefois, si vous avez besoin d’une prise en charge pour AppCache), IndexedDB, la géolocalisation ou l’accès par programmation au Presse-papiers, vous devrez continuer à utiliser <iframe> pour Windows 8.1.

Utilisation continue de <iframe> pour le contenu distant, une nouvelle entrée est requise dans le ApplicationContentUriRules de l’application. Les applications avec WebView requièrent de nouvelles entrées dans le ApplicationContentUriRules si le contenu Web doit appeler Window. external. notifier pour générer un événement [ScriptNotify](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) . Si vous n’avez pas Visual Studio, vous pouvez mettre à jour le manifeste de l’application en ajoutant le code XML suivant, y compris les caractères génériques pour les sous-domaines (par exemple, https:// \* . Microsoft.com) :


```
<Package>
    …
    <Applications>
        <Application>
            …
            <ApplicationContentUriRules>
                <Rule Match="https://www.example.com" Type="include"/>
            </ApplicationContentUriRules>
        </Application>
    </Applications>
</Package>
```



## <a name="resources"></a>Ressources

-   [ApplicationContentUriRules](/uwp/schemas/appxpackage/appxmanifestschema/element-applicationcontenturirules)
-   [<iframe>\| <iframe> objet élément](https://msdn.microsoft.com/library/windows/apps/hh465955.aspx)
-   [WebView (classe)](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041)
-   [WebView. ScriptNotify, événement](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041)

 

 