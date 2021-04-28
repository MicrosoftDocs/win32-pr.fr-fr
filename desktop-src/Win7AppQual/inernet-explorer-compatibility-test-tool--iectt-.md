---
description: Outil de test de compatibilité d'Internet Explorer (IECTT)
ms.assetid: 11169540-555A-48A9-A4CD-535D5765C005
title: Outil de test de compatibilité d'Internet Explorer (IECTT)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3a35b3120e95c668f2808c9c525d0c1d4f89f8f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088283"
---
# <a name="internet-explorer-compatibility-test-tool-iectt"></a>Outil de test de compatibilité d'Internet Explorer (IECTT)

L’outil de test de compatibilité d’Internet Explorer (IECTT) est un composant de [Microsoft Application Compatibility Toolkit](/windows-hardware/get-started/adk-install). Cet outil peut vous aider à diagnostiquer les problèmes dans vos applications Web en affichant des problèmes en temps réel et en chargeant éventuellement les résultats dans une base de données ACT. Les résultats incluent des détails sur les problèmes de compatibilité possibles et des liens pour plus d’informations sur chaque problème de compatibilité. IECTT vous permet également d’exclure des problèmes et de modifier les attributs disponibles.

## <a name="to-open-iectt"></a>Pour ouvrir IECTT

1.  Installez [Microsoft Application Compatibility Toolkit](/windows-hardware/get-started/adk-install).
2.  Cliquez sur **Démarrer**, pointez sur **programmes**, sur **Microsoft Application Compatibility Toolkit 5,6**, sur **outils de développement et** de test, puis cliquez sur outil de test de **compatibilité Internet Explorer**.

Les sections suivantes décrivent les scénarios de IECTT courants.

## <a name="view-issues-in-real-time"></a>Afficher les problèmes en temps réel

Vous pouvez rechercher et afficher vos problèmes Web en temps réel, pendant que vous testez vos sites Web et applications Web sur Windows Internet Explorer 7 et Windows Internet Explorer 8. Une fois vos tests terminés, vous pouvez afficher les résultats dans l’écran de **données dynamiques** de IECTT.

## <a name="upload-issues-to-your-act-database"></a>Télécharger des problèmes dans votre base de données ACT

Vous pouvez télécharger vos problèmes Web dans la base de données ACT, qui traite les informations et vous permet d’afficher vos résultats sur l’écran d' **analyse** du gestionnaire de compatibilité des applications.

## <a name="collect-your-compatibility-data"></a>Collecter vos données de compatibilité

Vous pouvez collecter les données de compatibilité de votre site Web et de vos applications Web à l’aide de l’outil IECTT avec Internet Explorer 7 ou Internet Explorer 7.

**Pour collecter vos données de compatibilité**

1.  Fermez toutes les fenêtres actives de Windows Internet Explorer.
2.  Dans IECTT, dans la barre d’outils de l' **outil de test de compatibilité d’Internet Explorer** , cliquez sur **activer**.
3.  Ouvrez une fenêtre Internet Explorer 7 ou Internet Explorer 8.

    Un message s’affiche et indique que la journalisation de l’évaluation de la compatibilité est activée.

4.  Visitez les sites Web ou les applications Web qui sont requis pour une utilisation par votre organisation. À mesure que vous visitez chaque site, l’outil IECTT affiche, en temps réel, vos problèmes de compatibilité potentiels.
5.  Dans la barre d’outils de l' **outil de test de compatibilité d’Internet Explorer** , cliquez sur **Désactiver** lorsque vous avez terminé.

    Le processus de journalisation de compatibilité se termine et s’arrête.

## <a name="filter-your-issue-results"></a>Filtrer les résultats de votre problème

Vous pouvez filtrer tous les résultats de votre IECTT par nom d’objet, par type de problème, ou par les deux.

**Pour filtrer les résultats de votre problème**

1.  Dans l’écran de l' **outil de test de compatibilité Internet Explorer** , cliquez sur **Filtrer**.

    La boîte de dialogue **filtre des problèmes** s’affiche.

2.  Entrez le nom de l’objet que vous souhaitez afficher dans la zone **Entrez le nom de l’objet pour lequel afficher les problèmes** .

Pour plus d’informations sur cet outil et d’autres outils de développement, consultez [qu’est-ce que l’outil de test de compatibilité d’Internet Explorer ?](/previous-versions/windows/it-pro/windows-7/cc721989(v=ws.10)) dans MSDN Library et le billet [de blog sur la journalisation des applications dans IE8](/archive/blogs/ie/application-compatibility-logging-in-ie8) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Outils de débogage d’applications Web et de modules complémentaires](tools-for-debugging-web-applications-and-add-ons.md)
</dt> </dl>

 

 
