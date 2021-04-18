---
description: Vue d’ensemble du modèle en cascade pour la classe RealTimeStylus.
ms.assetid: f4c377a7-979d-4a06-a8de-31b8e67d74f8
title: Modèle RealTimeStylus monté en cascade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2f61ea3cd44753d1d91fb2662226a716ee5590
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104557915"
---
# <a name="the-cascaded-realtimestylus-model"></a>Modèle RealTimeStylus monté en cascade

Le modèle [**RealTimeStylus**](realtimestylus-class.md) monté en cascade vous permet d’utiliser deux objets **RealTimeStylus** , chacun s’exécutant sur un thread différent. Avec ce modèle, vous attachez un objet **RealTimeStylus** secondaire à un objet **RealTimeStylus** principal. L’objet **RealTimeStylus** secondaire est attaché en tant que seul plug-in asynchrone dans la collection de plug-in asynchrone de l’objet **RealTimeStylus** principal.

Le modèle [**RealTimeStylus**](realtimestylus-class.md) monté en cascade peut être utile dans les scénarios suivants.

-   Vous pouvez ajouter certaines tâches qui peuvent être exigeantes en termes de calcul, tout en nécessitant un accès en temps réel au flux de données du stylet, tel que la reconnaissance de mouvement multitrait, à la collection de plug-ins synchrones de l’objet [**RealTimeStylus**](realtimestylus-class.md) secondaire.
-   Vous pouvez répartir la charge de calcul de vos plug-ins synchrones sur deux threads, ce qui réduit les retards dans la collecte d’encre sur certains Tablet PC.

Le diagramme suivant illustre le déroulement des données du stylet de tablette par le biais de deux objets [**RealTimeStylus**](realtimestylus-class.md) en cascade et de leurs collections de plug-ins.

![Illustration montrant le workflow de données RealTimeStylus en cascade](images/72ca1999-e078-49f8-a336-3b4d0157a472.gif)

Dans ce diagramme, le cercle « A » représente les données du stylet de tablette qui ont déjà été traitées par les objets [**RealTimeStylus**](realtimestylus-class.md) principal et secondaire et qui a été placé dans la file d’attente de sortie de l’objet **RealTimeStylus** secondaire. Le cercle « B » contient des données de stylet de tablette qui ont déjà été traitées par l’objet **RealTimeStylus** principal et ajoutées à la file d’attente de sortie de l’objet **RealTimeStylus** principal et qui n’ont pas encore été envoyées à l’objet **RealTimeStylus** secondaire. Le cercle « C » indique les données du stylet du Tablet PC actuellement traitées par l’objet **RealTimeStylus** principal. Il est envoyé à la collection de plug-ins synchrone et placé dans la file d’attente de sortie. Le cercle vide représente la position dans la file d’attente de sortie où les futures données de stylet du Tablet PC sont ajoutées.

## <a name="constraints"></a>Contraintes

Si vous utilisez le constructeur [**RealTimeStylus**](realtimestylus-class.md) par défaut, vous créez un objet **RealTimeStylus** qui peut uniquement accepter l’entrée d’un autre objet **RealTimeStylus** .

La liste suivante décrit les contraintes associées à l’utilisation du modèle [**RealTimeStylus**](realtimestylus-class.md) monté en cascade.

-   Seuls deux objets [**RealTimeStylus**](realtimestylus-class.md) peuvent être utilisés, un objet **RealTimeStylus** principal et un objet **RealTimeStylus** secondaire.
-   L’objet [**RealTimeStylus**](realtimestylus-class.md) primaire doit être créé avec un constructeur qui utilise le paramètre **attachedControl** ou *handle* . L’objet **RealTimeStylus** secondaire doit être créé avec le constructeur sans argument.
-   L’objet [**RealTimeStylus**](realtimestylus-class.md) secondaire doit être le seul plug-in asynchrone dans la collection de plug-in asynchrone de l’objet **RealTimeStylus** principal.
-   Un objet [**RealTimeStylus**](realtimestylus-class.md) secondaire ne peut être attaché qu’à un seul objet **RealTimeStylus** principal à la fois. Si elle est ajoutée à un deuxième objet **RealTimeStylus** principal, la méthode [Add](/previous-versions/ms824814(v=msdn.10)) lève une exception et l’objet **RealTimeStylus** secondaire n’est pas attaché au deuxième objet **RealTimeStylus** principal.
-   Le comportement de certains membres de l’objet [**RealTimeStylus**](realtimestylus-class.md) secondaire est modifié. Le tableau suivant décrit le comportement modifié de ces membres.

    

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Membre</th>
    <th>Comportement</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><a href="/previous-versions/ms825905(v=msdn.10)">GetDesiredPacketDescription</a></td>
    <td>Cette méthode retourne les informations de l’objet <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> principal.<br/> Si le <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> secondaire n’est pas attaché à un objet <strong>RealTimeStylus</strong> principal, cette méthode retourne la valeur par défaut.<br/></td>
    </tr>
    <tr class="even">
    <td><a href="/previous-versions/ms826041(v=msdn.10)">SetDesiredPacketDescription</a></td>
    <td>Cette méthode lève une exception <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> .<br/></td>
    </tr>
    <tr class="odd">
    <td><a href="/previous-versions/ms825913(v=msdn.10)">GetStyluses</a></td>
    <td>Cette méthode retourne les informations de l’objet <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> principal.<br/> Si le <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> secondaire n’est pas attaché à un objet <strong>RealTimeStylus</strong> principal, cette méthode retourne un tableau vide.<br/></td>
    </tr>
    <tr class="even">
    <td><a href="/previous-versions/ms824832(v=msdn.10)">Enabled</a></td>
    <td>L’obtention de cette propriété retourne les informations de l’objet <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> principal.<br/> Si le <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> secondaire n’est pas attaché à un objet <strong>RealTimeStylus</strong> principal, l’obtention de cette propriété retourne la valeur par défaut.<br/>
    <blockquote>
    [!Note]<br />
La définition de cette propriété lève une exception <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> .
    </blockquote>
    <br/></td>
    </tr>
    <tr class="odd">
    <td><a href="/previous-versions/ms824834(v=msdn.10)">WindowInputRectangle</a></td>
    <td>L’obtention de cette propriété retourne les informations de l’objet <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> principal.<br/> Si le <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> secondaire n’est pas attaché à un objet <strong>RealTimeStylus</strong> principal, l’obtention de cette propriété retourne la valeur par défaut.<br/>
    <blockquote>
    [!Note]<br />
La définition de cette propriété lève une exception <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> .
    </blockquote>
    <br/></td>
    </tr>
    </tbody>
    </table>

    

     

-   L’objet [**RealTimeStylus**](realtimestylus-class.md) parent est supposé cesser de fonctionner lorsque le **RealTimeStylus** enfant est supprimé.

 

 
