---
title: configuration requise pour que les lecteurs Audio portables s’affichent dans l’explorateur de Windows
description: configuration requise pour que les lecteurs Audio portables s’affichent dans l’explorateur de Windows
ms.assetid: 94227ed8-56e7-4366-9c38-9b5dbf907e16
keywords:
- Windows Gestionnaire de périphériques multimédia, lecteurs audio portables
- Gestionnaire de périphériques, lecteurs audio portables
- Guide de programmation, lecteurs audio portables
- fournisseurs de services, lecteurs audio portables
- création de fournisseurs de services, de lecteurs audio portables
- lecteurs audio portables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16d91e844f564ead03ddb78cf57c13c81a56bc8934bbfbde51c105b5c7e1e2f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055577"
---
# <a name="requirements-for-portable-audio-players-to-appear-in-windows-explorer"></a>configuration requise pour que les lecteurs Audio portables s’affichent dans l’explorateur de Windows

l’extension de l’espace de noms du shell de lecteur audio portable offre aux utilisateurs Windows un moyen cohérent de gérer les périphériques audio gérés par Windows Gestionnaire de périphériques multimédia. Si vous créez votre fournisseur de services et vos composants de pilote conformément aux instructions suivantes, votre appareil s’affiche dans l’espace de noms Shell. les utilisateurs peuvent interagir avec le contenu de votre appareil de manière cohérente dans Windows Explorer pour effectuer des opérations de base telles que copier, supprimer et renommer.

les spécifications de l’interpréteur de commandes suivantes pour le fournisseur de services et les composants de pilote sont destinées à compléter les instructions générales relatives à la Gestionnaire de périphériques Windows Media.

Fonctionnalités de l’appareil

Windows Les fournisseurs de services Media Gestionnaire de périphériques doivent être explicites dans leurs fonctionnalités prises en charge. Si un appel n’est pas pris en charge, un code d’erreur doit être retourné. Les champs appropriés doivent être définis pour la présence ou l’absence de fonctionnalités au retour des fonctions suivantes :

-   [**IMDSPStorageGlobals :: GetCapabilities**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getcapabilities)
-   [**IMDSPStorage :: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getattributes)
-   [**IMDSPDevice::GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getformatsupport)

Les fournisseurs de services doivent prendre en charge les fonctionnalités suivantes pour être compatibles avec l’interpréteur de commandes :

-   Copier sur l’appareil (avec prise en charge des rappels d’annulation et de progression)
-   Supprimer le fichier de l’appareil (avec prise en charge des rappels d’annulation et de progression)
-   Renommer le fichier sur l’appareil
-   Rapport d’espace (espace total, espace libre, espace inutilisable)
-   Plug-and-Play (voir [activation de PNP pour les appareils](enabling-pnp-for-devices.md))
-   Format (de préférence avec prise en charge des rappels d’annulation et de progression)

Si les métadonnées sont prises en charge, les champs suivants doivent être pris en charge pour les fichiers individuels. Si aucune donnée n’est disponible, le champ doit être initialisé en tant que chaîne vide :



| Champ        | Constante (définie dans WMDM. idl) | Balise Metadata    |
|--------------|--------------------------------|-----------------|
| Titre de la chanson   | \_wszWMDMTitle g                | WMDM/titre      |
| Numéro de suivi | \_wszWMDMTrack g                | WMDM/suivi      |
| Peinture       | \_wszWMDMAuthor g               | WMDM/auteur     |
| Album        | \_wszWMDMAlbumTitle g           | WMDM/AlbumTitle |
| Year         | \_wszWMDMYear g                 | WMDM/an       |
| Genre        | \_wszWMDMGenre g                | WMDM/genre      |



 

Accès concurrentiel

les pilotes en mode noyau pour Windows Media Gestionnaire de périphériques doivent être robustes pour gérer l’accès simultané. Par exemple, un utilisateur peut accéder simultanément à l’appareil à l’aide de l’interpréteur de commandes et du lecteur multimédia, ou simplement à l’aide de plusieurs fenêtres dans l’interpréteur de commandes. Dans le cadre de la gestion de l’accès concurrentiel, les pilotes ne doivent pas supposer, juste parce que le fournisseur de services est chargé, que l’appareil est en cours d’utilisation. Au lieu de cela, ils doivent implémenter un mécanisme de verrouillage pour sérialiser l’accès à l’appareil en fonction des besoins des opérations individuelles.

Interface utilisateur du service

les fournisseurs de services pour Windows Media Gestionnaire de périphériques ne doivent afficher aucune interface utilisateur. toutes les erreurs doivent être retournées à partir des appels de méthode en tant que Windows spécifique Gestionnaire de périphériques les codes d’erreur dans la mesure du possible.

Activation dans l’interpréteur de commandes

Si votre package remplit toutes les conditions requises de l’interpréteur de commandes, vous pouvez autoriser l’affichage de votre appareil dans l’interpréteur de commandes en définissant la valeur *ShowInShell* sur 1 sous les paramètres de l’appareil. Pour plus d’informations, consultez Paramètres de l' [appareil](device-parameters.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création d’un fournisseur de services**](creating-a-service-provider.md)
</dt> </dl>

 

 




