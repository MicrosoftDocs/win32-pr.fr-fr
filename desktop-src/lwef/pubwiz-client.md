---
title: Conception de Client-Side
description: Le script des pages HTML côté serveur communique avec le client de l’Assistant commande d’impression en ligne dans lequel il est hébergé. Cette communication s’effectue par le biais de méthodes et de propriétés accessibles par l’objet Window. external.
ms.assetid: fa76ccee-0b94-41b5-8cc8-eb7e1818dbed
keywords:
- assistants de publication, conception côté client
- Window. external, assistants de publication
- assistants de publication, Window. external
- assistants de publication, considérations relatives à la conception
- assistants de publication, Assistant commande d’impression en ligne
- Assistant commande d’impression en ligne, conception côté client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c40aafc7a08820125df222c1c6d911b0d2b4d0a1fb625b7c62fc6d4be8bebd7c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665079"
---
# <a name="client-side-design"></a>Conception de Client-Side

Le script des pages HTML côté serveur communique avec le client de l’Assistant commande d’impression en ligne dans lequel il est hébergé. Cette communication s’effectue par le biais de méthodes et de propriétés accessibles par l’objet **Window. external** .

Les rubriques suivantes sont traitées dans ce document.

-   [Méthodes et propriétés](#methods-and-properties)
-   [Remarques sur la conception](#design-considerations)
-   [Rubriques connexes](#related-topics)

## <a name="methods-and-properties"></a>Méthodes et propriétés

Les méthodes et propriétés suivantes sont disponibles via l’objet **Window. external** .

-   [**FinalBack**](/windows/desktop/shell/iwebwizardhost-finalback)
-   [**FinalNext**](/windows/desktop/shell/iwebwizardhost-finalnext)
-   [**Annuler**](/windows/desktop/shell/iwebwizardhost-cancel)
-   [**PassportAuthenticate**](/windows/desktop/shell/inewwdevents-passportauthenticate)
-   [**SetHeaderText**](/windows/desktop/shell/iwebwizardhost-setheadertext)
-   [**SetWizardButtons**](/windows/desktop/shell/iwebwizardhost-setwizardbuttons)
-   [**Caption**](/previous-versions/windows/desktop/legacy/bb774352(v=vs.85))
-   [**Propriété**](/windows/desktop/shell/iwebwizardhost-property)

Le script de la page côté serveur appelle ces méthodes pour notifier le client des événements au cours de la procédure de publication. Prenons l’exemple de [**FinalBack**](/windows/desktop/shell/iwebwizardhost-finalback) . Lorsque l’Assistant affiche la première page HTML côté serveur, il s’occupe de la connaissance des handles des pages d’Assistant précédentes et des pages HTML hébergées. À ce stade de notre exemple, l’utilisateur, assis sur la première page HTML, clique sur le bouton **précédent** . L’Assistant envoie une notification de cet événement au serveur. À la réception de ce message, le script côté serveur fait référence à son gestionnaire **OnBack** pour cet événement, qui, comme il s’agit de la première page HTML, appelle la méthode **FinalBack** . L’Assistant accède alors à la page de l’Assistant affichée avant d’entrer dans l’interface utilisateur côté serveur.

Pour une description complète de ces méthodes et propriétés, consultez la documentation relative aux objets [**WebWizardHost**](/windows/desktop/shell/webwizardhost) et [**NewWDEvents**](/windows/desktop/shell/newwdevents) .

## <a name="design-considerations"></a>Remarques sur la conception

Le code HTML qui compose chaque page côté serveur s’affiche normalement dans le volet de l’Assistant. Lorsque vous concevez ces pages, gardez à l’esprit qu’une fenêtre d’Assistant ne peut pas être redimensionnée. Les pages doivent donc être construites et dimensionnées de sorte que les barres de défilement soient évitées chaque fois que possible pour fournir à l’utilisateur une navigation lisse dans l’Assistant.

Chaque page HTML doit également fournir un gestionnaire pour les événements **OnBack**, **OnNext** et **OnCancel** . Le gestionnaire **OnNext** gère également l’événement **Finish** . Une page qui n’implémente pas une fonction **OnBack** n’est pas considérée comme non valide et entraîne l’affichage d’une page d’erreur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**WebWizardHost**](/windows/desktop/shell/webwizardhost)
</dt> <dt>

[**NewWDEvents**](/windows/desktop/shell/newwdevents)
</dt> <dt>

[Conception côté serveur](pubwiz-server.md)
</dt> </dl>

 

 