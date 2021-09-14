---
title: Direct2D
description: Direct2D
ms.assetid: 03b3b91c-9751-4f8d-af24-85067f06930b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8223ec5e98db3e45b0087073b4eb68baeae81280
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127113309"
---
# <a name="direct2d"></a>Direct2D

## <a name="purpose"></a>Objectif

Direct2D est une API graphique 2D à accélération matérielle et en mode immédiat, qui offre des performances élevées et un rendu de grande qualité pour les éléments géométriques, bitmaps et textes 2D. l’API Direct2D est conçue pour interagir correctement avec GDI, GDI+ et Direct3D.

## <a name="developer-audience"></a>Développeurs concernés

Direct2D est principalement conçu pour être utilisé par les classes de développeurs suivantes :

-   Développeurs de grandes applications natives à l’échelle de l’entreprise.
-   Les développeurs qui créent des outils de contrôle et des bibliothèques pour la consommation par les développeurs en aval.
-   Développeurs qui ont besoin d’un rendu côté serveur d’un graphique 2D.
-   Les développeurs qui utilisent les graphiques Direct3D et ont besoin d’un rendu de texte et de langage 2D simple et hautes performances pour les menus, les éléments d’interface utilisateur et les affichages des têtes (HUDs).

## <a name="run-time-requirements"></a>Conditions d’exécution

-   Windows 7 ou Windows vista avec Service Pack 2 (SP2) et la mise à jour de la plateforme pour Windows Vista et versions ultérieures.
-   Windows server 2008 R2 ou Windows server 2008 avec Service Pack 2 (SP2) et la mise à jour de la plateforme pour Windows Server 2008 et versions ultérieures.

> [!Note]
>
> la mise à jour de la plateforme pour Windows Vista et la mise à jour de la plateforme pour Windows Server 2008 est un ensemble de bibliothèques runtime qui permet aux développeurs de cibler des applications sur Windows 7, Windows Vista, Windows server 2008 R2 et Windows server 2008. ces mises à jour seront disponibles pour tous les clients Windows Vista et Windows Server 2008 par le biais de Windows Update. les applications tierces qui requièrent la mise à jour de la plateforme pour Windows Vista ou la mise à jour de la plateforme pour Windows Server 2008 peuvent avoir Windows Update détecter si la mise à jour requise est installée ; si ce n’est pas le cas, Windows Update le télécharge et l’installe en arrière-plan. pour plus d’informations sur les deux mises à jour, consultez [mise à jour de la plateforme pour Windows Vista](https://support.microsoft.com/kb/971644).

 

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                          | Description                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Nouveautés de Direct2D](what-s-new-in-direct2d-for-windows-8-consumer-preview.md)<br/> | Voici quelques-uns des nouveaux ajouts à Direct2D. <br/>                                                                                                                   |
| [À propos de Direct2D](direct2d-overview.md)<br/>                                             | Introduit Direct2D, une API qui fournit aux développeurs Win32 la possibilité d’effectuer des tâches de rendu graphiques 2D avec des performances et une qualité visuel supérieures. <br/> |
| [Démarrage rapide de Direct2D pour Windows 8](direct2d-quickstart-with-device-context.md)<br/>    | Résume les étapes requises pour dessiner avec Direct2D et fournit un exemple de code.<br/>                                                                                     |
| [Prise en main avec Direct2D](getting-started-with-direct2d-nav.md)<br/>              | Décrit comment prendre en main la création d’applications Direct2D et fournit un exemple de code.<br/>                                                                             |
| [Guide de programmation](programming-guide.md)<br/>                                          | Cette section contient des rubriques de programmation conceptuelle qui décrivent comment utiliser l’API Direct2D. <br/>                                                                    |
| [Référence Direct2D](reference.md)<br/>                                                      | Décrit en détail l’API Direct2D.<br/>                                                                                                                              |
| [Outils et utilitaires](tools-and-utilities.md)<br/>                                      | Outils et utilitaires fournis pour Direct2D.<br/>                                                                                                                         |
| [Exemples](d2d-samples.md)<br/>                                                          | Exemples d’applications qui illustrent l’API Direct2D.<br/>                                                                                                             |
| [Glossaire Direct2D](direct2d-glossary.md)<br/>                                          | Décrit les termes couramment utilisés par la documentation Direct2D. <br/>                                                                                                      |



 

## <a name="additional-resources"></a>Ressources supplémentaires

-   [**Graphiques et jeux DirectX**](/windows/desktop/directx)
-   [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal)

 

