---
title: Activation de la journalisation
description: Activation de la journalisation
ms.assetid: 50fc1d71-b650-4ba5-a6e1-631c0b9fe8ad
keywords:
- Windows Gestionnaire de périphériques de média, journalisation
- Gestionnaire de périphériques, journalisation
- applications de bureau, journalisation
- fournisseurs de services, journalisation
- Guide de programmation, journalisation
- journalisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ff937b2a3abd16f7319c3abb73a3a2159350049fff8c89d343cc5545f8a21ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585117"
---
# <a name="enabling-logging"></a>Activation de la journalisation

Windows Le Gestionnaire de périphériques de média fournit un objet de journalisation qui peut enregistrer des informations dans un fichier texte au moment de l’exécution. Les développeurs des applications et des fournisseurs de services peuvent utiliser cet objet pour stocker des messages dans un fichier journal pendant l’exécution de leur application ou du fournisseur de services. cet objet est particulièrement utile lors de la gestion des fichiers protégés par drm, car Windows Media Gestionnaire de périphériques ne vous permet pas de joindre un débogueur à un processus qui gère des fichiers protégés par drm.

L’enregistreur d’événements est un objet COM avec l’ID de classe CLSID \_ WMDMLogger qui expose une interface, [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger). Les composants n’ont pas besoin d’un certificat pour utiliser l’objet de journalisation.

par défaut, Windows Media Gestionnaire de périphériques gère un fichier journal, qu’une application utilise ou non **IWMDMLogger**. Ce fichier journal est un fichier texte simple, et chaque entrée comprend une entrée précédée d’un horodatage au format aaaammjjhhmmss, utilisant une heure locale de 24 heures. Windows Media Gestionnaire de périphériques journalise tous les appels d’API, ainsi que toutes les entrées que vous ajoutez en appelant des messages **IWMDMLogger** . Toutes les entrées de fichier journal sont ajoutées au fichier jusqu’à ce que la [**réinitialisation**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-reset) soit appelée ou que le fichier dépasse sa taille maximale. Le fichier est fermé automatiquement après chaque opération de journalisation. Le même fichier journal est utilisé pour les entrées d’application et les entrées système.

Les étapes suivantes montrent comment utiliser l’objet de journalisation :

1.  Incluez wmdmlog. h dans votre projet.
2.  Créez un objet de journalisation en appelant **CoCreateInstance**(CLSID \_ WMDMLogger) et en demandant l’interface **IWMDMLogger** . Assignez le pointeur d’interface à une variable globale.
3.  Vérifiez que la journalisation est activée en appelant [**IWMDMLogger :: IsEnabled**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-isenabled); Si ce n’est pas le cas, activez-le en appelant [**IWMDMLogger :: Enable**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-enable).
4.  Spécifiez un nom et une taille de fichier journal personnalisés. Pour ce faire, appelez [**IWMDMLogger :: SetLogFileName**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-setlogfilename) et [**IWMDMLogger :: SetSizeParams**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-setsizeparams).
5.  À des points de votre code où vous souhaitez créer une entrée dans le journal, appelez [**IWMDMLogger :: LogDword**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-logdword) pour consigner des chaînes contenant des variables (cette méthode est similaire à **wsprintf** dans le sens où elle vous permet de mettre en forme une chaîne contenant une valeur de variable), ou appelez [**IWMDMLogger :: LogString**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-logstring) pour enregistrer des chaînes constantes.

Pour obtenir un exemple de code, consultez les pages de référence pour les méthodes de [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Tâches communes aux applications et aux fournisseurs de services**](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 




