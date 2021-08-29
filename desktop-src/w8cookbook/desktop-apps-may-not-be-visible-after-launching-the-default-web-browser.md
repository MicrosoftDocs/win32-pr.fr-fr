---
title: les applications de bureau peuvent ne pas être visibles après le lancement du navigateur web par défaut ou des applications du windows Store Windows
description: les applications de bureau peuvent ne pas être visibles après le lancement du navigateur web par défaut ou des applications du windows Store Windows
ms.assetid: 5D2CE14B-111D-4987-A9AA-B04AC030F9F0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15eb77ad2876de352e8a3d9708040ccfabd8fefa5eb145941e7970c51cfc6588
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119549768"
---
# <a name="desktop-apps-may-not-be-visible-after-launching-the-default-web-browser-or-windows-store-apps"></a>les applications de bureau peuvent ne pas être visibles après le lancement du navigateur web par défaut ou des applications du windows Store Windows

## <a name="platforms"></a>Plateformes

**Clients** – Windows 8  
**serveurs** – Windows Server 2012  


## <a name="description"></a>Description

l’expérience utilisateur de l’application Windows Store est axée sur une seule application à la fois, avec des tâches multitâches, de changement d’application et de notifications fournies par l’interface utilisateur Windows. Windows Les applications du Store sont dimensionnées pour occuper de l’espace disponible sur l’écran, avec la vue la plus courante en plein écran. Par conséquent, lorsqu’une autre application sur le système est lancée, vous ne pouvez plus supposer que la nouvelle application s’ouvre dans une fenêtre de bureau en même temps que votre application de bureau. c’est toujours le cas des applications et navigateurs Windows du windows Store qui choisissent de participer au nouvel Windows interface utilisateur. Vous pouvez continuer à voir d’autres applications en même temps, par exemple, si vous êtes sur le bureau et lancez une autre application de bureau ou si vous avez des applications dans un état d’alignement.

## <a name="manifestation"></a>Manifestation

quand une application de bureau utilise des techniques d’activation d’application courantes telles que l’utilisation de l’API ShellExecute sur un fichier ou un protocole, Windows lance l’application associée à cette inscription, qui peut être une application Windows Store et/ou le navigateur web par défaut de l’utilisateur (le navigateur web par défaut peut choisir de participer au bureau ou à la nouvelle interface utilisateur du Windows). Windows Les applications du Windows Store sont lancées en mode plein écran, en masquant le bureau et l’application de bureau à partir de laquelle elles ont été lancées.

> [!Note]  
> dans Windows 8, Internet Explorer 10 est configuré en tant que navigateur par défaut de l’utilisateur, mais l’utilisateur peut choisir d’installer et de définir un autre navigateur comme navigateur par défaut (aucune modification par rapport à Windows 7). dans Internet Explorer 10, lorsqu’un lien est ouvert à partir d’une application de bureau, Internet Explorer s’ouvre sur le bureau. toutefois, ce paramètre peut être modifié par les utilisateurs afin qu’Internet Explorer s’ouvre en tant qu’application Windows Store. Les fournisseurs de navigateurs ont été encouragés à adopter une expérience de « lancement contextuel » similaire. Toutefois, les développeurs doivent prévoir le fait que tous les navigateurs ne se comportent pas de la même façon.

 

## <a name="mitigation"></a>Limitation des risques

Bien qu’il n’y ait aucune modification que les développeurs peuvent apporter à leurs applications pour atténuer ce comportement, l’utilisateur final peut faire en sorte qu’il puisse communiquer avec eux. Envisagez d’utiliser les informations collectées par l’API ShellExecuteEx () étendue pour remplir une boîte de dialogue appropriée. dans cette boîte de dialogue, indiquez à l’utilisateur quelle application sera lancée et si cette application est une application Windows Store ou une application de bureau. le CLSID peut être utilisé pour distinguer Windows applications du windows store des applications de bureau. Options de l’utilisateur :

-   les utilisateurs qui disposent d’un moniteur à écran étendu peuvent aligner l’application Windows store sur le bord de l’écran pour exposer le bureau et ainsi afficher l’application Windows store et l’application de bureau en même temps.
-   Si Internet Explorer est configuré en tant que navigateur par défaut de l’utilisateur, les utilisateurs peuvent modifier son comportement en modifiant les options Internet dans le panneau de configuration. Dans l’onglet programmes, les utilisateurs peuvent modifier la manière dont Internet Explorer gère les liens. D’autres navigateurs peuvent offrir un paramètre similaire.

 

 




