---
description: Cette section décrit comment imprimer à partir d’un programme Windows natif.
ms.assetid: D0AE8FF8-D02D-43D3-80CA-E13EAA894F87
title: 'Comment : imprimer à partir d’un programme Windows'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84229823944d7f7104da359b953e579f1b21cdca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518915"
---
# <a name="how-to-print-from-a-windows-program"></a>Comment : imprimer à partir d’un programme Windows

Cette section décrit comment imprimer à partir d’un programme Windows natif.

## <a name="overview"></a>Vue d’ensemble

L’impression fait généralement partie intégrante d’un programme Windows natif. Par conséquent, il ne s’agit pas d’une fonctionnalité que vous pouvez ajouter facilement après avoir écrit le programme. Cela dit, si le programme est conçu pour utiliser des documents XPS, il n’aura pas besoin d’une grande quantité de code pour afficher le contenu du document en vue de son impression. Les documents XPS de l’application peuvent être envoyés directement à une imprimante disposant d’un pilote d’imprimante XPSDrv.

Utilisez l' [API de document XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)) pour créer le contenu du document et l' [API d’impression XPS](xps-printing.md) pour envoyer le contenu du document à l’imprimante. L’API d’impression XPS traite le contenu du document pour l’imprimante de destination. Si l’imprimante sélectionnée possède un pilote d’imprimante XPSDrv, le document est envoyé à l’imprimante sans conversion supplémentaire. Si l’imprimante sélectionnée possède un pilote d’imprimante GDI, le programme peut également envoyer le contenu à l’imprimante, et l’API d’impression XPS convertit le contenu du document afin qu’il soit compatible avec le pilote d’imprimante GDI. Dans les deux cas, le traitement effectué par l’application est le même.

## <a name="printing-tasks"></a>Tâches d’impression

Les rubriques suivantes décrivent les étapes de base de l’impression du contenu d’un programme.

1.  **Collecter les informations de travail d’impression de l’utilisateur.**

    En règle générale, un utilisateur lance un travail d’impression lorsqu’il sélectionne l’option d’impression dans un menu et le programme affiche une boîte de dialogue Imprimer pour collecter les détails du travail d’impression. L’utilisateur sélectionne généralement l’imprimante, le nombre de copies et les détails de configuration de l’imprimante, tels que l’impression recto verso et l’agrafage.

    Pour plus d’informations sur la procédure à suivre, consultez [Comment : collecter des informations de travail d’impression à partir de l’utilisateur](preparing-to-print.md).

2.  **Créer un indicateur de progression.**

    Un indicateur de progression fournit à l’utilisateur des commentaires sur la progression du travail d’impression. L’indicateur de progression peut être une barre de progression qui fait partie d’une boîte de dialogue qui comprend le bouton **Annuler** pour le travail, ou il peut s’agir d’une barre de progression dans la barre d’État en bas de la fenêtre principale.

    Pour plus d’informations sur le fonctionnement de l’indicateur de progression, consultez [procédure : afficher la progression du travail d’impression](cancel-dialog-box.md).

    Pour plus d’informations sur l’affichage de la progression du travail d’impression, consultez les informations dans les instructions de développement de l' [interface utilisateur de l’application Windows](/windows/desktop/windows-application-ui-development) .

3.  **Démarrez le thread d’impression.**

    Une fois que le programme a collecté les informations du travail d’impression auprès de l’utilisateur, il peut démarrer le thread d’impression pour effectuer le traitement réel du document en vue de l’impression.

    Pour plus d’informations sur le thread d’impression, consultez [procédure : Démarrer et arrêter un thread d’impression](how-to--start-and-stop-a-printing-thread.md).

4.  **Affichez les données du travail d’impression.**

    Le thread d’impression restitue les données du document pour l’impression. Vous devez décomposer ce traitement en étapes de traitement discrètes afin que l’utilisateur puisse interrompre le traitement et annuler le travail, ainsi que pour ne pas autoriser le thread de traitement à bloquer d’autres threads et processus.

    Pour plus d’informations sur le rendu des données du travail d’impression, consultez [Comment : afficher des données de travail d’impression](how-to--render-the-print-job-data.md).

5.  **Surveiller la progression du travail d’impression.**

    À mesure que chaque étape de traitement est effectuée, mettez à jour la barre de progression pour informer l’utilisation. Calculez les étapes de traitement pour terminer la tâche demandée, puis mettre à jour la barre de progression à mesure que ces étapes sont effectuées.

6.  **Fermer le travail d’impression et terminer le thread d’impression.**

    Une fois que le programme a envoyé le travail d’impression à l’imprimante, ou si l’utilisateur a annulé le travail d’impression, vous devez fermer le travail d’impression et libérer les ressources utilisées par le travail d’impression.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Procédure : collecter des informations de travail d’impression à partir de l’utilisateur](preparing-to-print.md)
</dt> </dl>

 

 
