---
title: Conception de Server-Side
description: Les fonctions côté serveur communiquent avec l’Assistant client via l’objet Windows. external. Le script côté serveur fournit ces fonctions pour répondre aux événements de l’Assistant et récupérer des informations sur l’Assistant.
ms.assetid: 7cc8b814-f230-4326-a9df-a491ed35483e
keywords:
- assistants de publication, conception côté serveur
- Window. external, assistants de publication
- assistants de publication, Window. external
- assistants de publication, fonctions de script de navigation
- scripts, assistants de publication
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20b3b218bbca297be446016335d90fe717a88bba
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118174"
---
# <a name="server-side-design"></a>Conception de Server-Side

Les fonctions côté serveur communiquent avec l’Assistant client via l’objet **Windows. external** . Le script côté serveur fournit ces fonctions pour répondre aux événements de l’Assistant et récupérer des informations sur l’Assistant.

Les rubriques suivantes sont traitées dans ce document.

-   [Implémentation de fonctions de script de navigation](#implementing-navigation-script-functions)
    -   [OnBack()](#onback)
    -   [OnNext ()](#onnext)
    -   [OnCancel ()](#oncancel)
-   [Autres méthodes et propriétés](#other-methods-and-properties)
    -   [Méthodes](#methods)
    -   [Propriétés](#properties)
-   [Rubriques connexes](#related-topics)

## <a name="implementing-navigation-script-functions"></a>Implémentation de fonctions de script de navigation

Le script côté serveur dans chaque page HTML répond aux boutons de navigation par le biais de fonctions pour **OnBack**, **OnNext** et **OnCancel**. Ces fonctions doivent être accessibles via **IHTMLDocument :: obten \_ script** sur le client et ne prennent pas de paramètres.

### <a name="onback"></a>OnBack()

-   Répond lorsque l’utilisateur clique sur **précédent** dans l’Assistant.
-   Si la page côté serveur Active est la première page côté serveur, appelez **Window. external. FinalBack** pour indiquer au client d’accéder à la page précédente côté client.
-   Si la page côté serveur active n’est pas la première page côté serveur, accédez à la page précédente côté serveur.
-   Cette fonction doit être implémentée pour chaque page. Toute page qui ne parvient pas à le faire est considérée comme non valide et affiche une page d’erreur.

### <a name="onnext"></a>OnNext ()

-   Répond quand l’utilisateur clique sur **suivant** dans l’Assistant.
-   Si la page côté serveur Active est la dernière page côté serveur, appelez **Window. external. FinalNext** pour indiquer au client d’accéder à la page suivante côté client ou de terminer l’Assistant.
-   Si la page côté serveur active n’est pas la dernière page côté serveur, accédez à la page suivante côté serveur.

### <a name="oncancel"></a>OnCancel ()

-   Répond quand l’utilisateur clique sur **Annuler** dans l’Assistant.
-   L’interface utilisateur doit être conçue pour permettre à l’utilisateur d’annuler à tout moment.
-   Une fois que le traitement de la fonction **OnCancel** est traité, le client ferme l’Assistant.

## <a name="other-methods-and-properties"></a>Autres méthodes et propriétés

Les fonctions implémentées par le client sont accessibles via **Windows. external**, comme les propriétés. Les services disponibles sont les suivants :

### <a name="methods"></a>Méthodes

-   [**SetHeaderText**](/windows/desktop/shell/iwebwizardhost-setheadertext)
-   [**SetWizardButtons**](/windows/desktop/shell/iwebwizardhost-setwizardbuttons)
-   [**PassportAuthenticate**](/windows/desktop/shell/inewwdevents-passportauthenticate)

### <a name="properties"></a>Propriétés

-   [**Caption**](/previous-versions/windows/desktop/legacy/bb774352(v=vs.85))
-   [**Propriété**](/windows/desktop/shell/iwebwizardhost-property)

L’exemple de code suivant montre le code côté serveur d’une page d’assistant simple qui implémente la page d’erreur du service Web.


```
<html>
    <head>
        <script language="JavaScript">
            function window.onload()
            {
                window.external.SetWizardButtons(1, 0, 0);    
                <!-- Back button enabled -->
            }

            function window.onback()
            {
                window.external.FinalBack();
            }
        </script>
    </head>
.
.
.
</html>
                    
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Conception côté client](pubwiz-client.md)
</dt> <dt>

[Inscription d’un service](pubwiz-reg.md)
</dt> </dl>

 

 