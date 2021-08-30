---
title: principaux outils et Techniques pour créer des jeux Windows plus robustes
description: Cet article décrit les outils et techniques que vous pouvez utiliser pour réduire le nombre d’appels au support technique que vous recevez.
ms.assetid: ad3d100c-4f87-f1e4-3242-8b2052ba171d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecee561149063ba80e47c2b6560441bebf6c851a61187cc9fbbd9e3278e71686
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901989"
---
# <a name="top-tools-and-techniques-for-making-more-robust-windows-games"></a>principaux outils et Techniques pour créer des jeux Windows plus robustes

L’un des coûts les plus indésirables pour la production de jeux est le support des appels. Chaque fois qu’un utilisateur contacte le support technique, le bénéfice du jeu est réduit. Bien que certains appels au support client ne soient pas empêchables, d’autres peuvent être éliminés ou réduits en utilisant des pratiques de développement efficaces. Cet article décrit les outils et techniques que vous pouvez utiliser pour réduire le nombre d’appels au support technique que vous recevez.

Tous les outils décrits ici sont gratuits, et les techniques sont suffisamment simples pour s’ajouter à la plupart des méthodes de développement.

Outils et techniques :

-   [PREfast](#prefast)
-   [AppVerifier](#appverifier)
-   [Shared Computer Toolkit de compatibilité des applications Microsoft](#microsoft-application-compatibility-toolkit)
-   [Test de la protection des comptes d’utilisateur](#user-account-protection-testing)
-   [PIX pour Windows](#pix-for-windows)
-   [Détection de la configuration](#configuration-detection)
-   [Activer les avertissements complets du compilateur](#enable-full-compiler-warnings)
-   [Serveur de symboles Microsoft](#microsoft-symbol-server)
-   [Rapport d’erreurs Windows](#windows-error-reporting)
-   [Outils de réglage des performances](#performance-tuning-tools)
-   [Résumé](#summary)

## <a name="prefast"></a>PREfast

PREfast for drivers est un outil proposé par Microsoft qui analyse les chemins d’exécution en C ou C++ compilé pour faciliter la recherche des bogues au moment de l’exécution. PREfast fonctionne en utilisant tous les chemins d’exécution dans toutes les fonctions et en évaluant chaque chemin d’accès pour résoudre les problèmes. Bien que cet outil soit normalement utilisé pour développer des pilotes et d’autres codes de noyau, il peut aider les développeurs de jeux à gagner du temps en éliminant les bogues difficiles à trouver ou ignorés par le compilateur. L’utilisation de PREfast est un excellent moyen de réduire la charge de travail après la publication et les coûts de support.

prefast est fourni avec Visual Studio Team System et dans le cadre de [Windows Driver Kit](https://www.microsoft.com/whdc/devtools/WDK/). Pour plus d’informations sur PREfast, consultez [PREfast for drivers](https://www.microsoft.com/whdc/devtools/tools/PREfast.mspx).

## <a name="appverifier"></a>AppVerifier

Le Application Verifier Microsoft, ou AppVerifier, est un outil qui peut aider les testeurs en fournissant plusieurs fonctions dans un seul outil. AppVerifier a été développé pour faciliter le test des erreurs de programmation courantes. AppVerifier peut vérifier les paramètres qui sont transmis dans les appels d’API, injecter une entrée erronée pour vérifier la capacité de gestion des erreurs et enregistrer les modifications dans le registre et le système de fichiers. AppVerifier peut également détecter les dépassements de mémoire tampon dans le segment de mémoire, vérifier qu’une liste de contrôle d’accès (ACL) a été correctement définie et appliquer l’utilisation sécurisée des API de Sockets.

Bien qu’il ne soit pas exhaustif, AppVerifier peut faire partie d’un autre composant de la boîte à outils d’un testeur pour permettre à un studio de développement de publier un produit de qualité et de réduire les coûts potentiels de la publication.

Pour plus d’informations sur Application Verifier, consultez [Application Verifier](/previous-versions/ms220948(v=vs.80)) et [utilisation de Application Verifier dans le cycle de vie du développement de logiciels](/previous-versions/aa480483(v=msdn.10)) sur MSDN. Vous pouvez télécharger Application Verifier à partir des [Détails du téléchargement : Application Verifier](https://www.microsoft.com/download/details.aspx?id=20028) sur le centre de téléchargement Microsoft.

Un outil similaire pour les pilotes, le vérificateur de pilotes, est également disponible. pour plus d’informations, consultez [utilisation du vérificateur de pilotes pour identifier les problèmes liés aux pilotes Windows pour les utilisateurs expérimentés](https://support.microsoft.com/Default.aspx?kbid=244617) sur le centre d’aide et de Support Microsoft.

## <a name="microsoft-application-compatibility-toolkit"></a>Shared Computer Toolkit de compatibilité des applications Microsoft

le Shared Computer Toolkit de compatibilité des applications Microsoft est un ensemble d’outils gratuits pour aider les développeurs à vérifier rapidement comment leurs mises en production seront exécutées sur les nouveaux service packs pour Microsoft Windows. En étant prêt pour les nouveaux service packs, les développeurs peuvent empêcher ou être prêts pour des problèmes.

pour plus d’informations sur la compatibilité des applications Shared Computer Toolkit, consultez [Windows compatibilité des applications](https://www.microsoft.com/technet/prodtechnol/windows/appcompatibility/default.mspx).

## <a name="user-account-protection-testing"></a>Test de la protection des comptes d’utilisateur

Windows Vista et Windows 7 ont deux types principaux de comptes d’utilisateur : utilisateur Standard et administrateur. Les comptes d’utilisateur standard sont le type préféré pour tous les utilisateurs, car ils réduisent le risque d’endommagement du système par des applications malveillantes. Étant donné que l’utilisateur standard a des restrictions d’accès, telles que le fait de ne pas pouvoir écrire dans le dossier Program Files ou sur HKEY \_ local \_ machine (HKLM) dans le registre, il est important que les jeux soient conçus et testés pour fonctionner avec un compte d’utilisateur standard.

pour plus d’informations sur cette rubrique, consultez les articles [correctifs logiciels de jeu dans Windows XP, Windows Vista et Windows 7](./patching-methods-in-windows-xp-and-vista.md) et [contrôle de compte d’utilisateur pour les développeurs de jeux](./user-account-control-for-game-developers.md).

## <a name="pix-for-windows"></a>PIX pour Windows

PIX est un outil permettant de collecter et d’analyser les informations de performances d’une application en cours d’exécution. PIX peut collecter des données statistiques sur la raison pour laquelle certains frames s’affichent plus lentement que d’autres et peuvent identifier une mauvaise utilisation des API. PIX peut également être automatisé pour tester la génération quotidienne et signaler les changements soudains dans les performances de l’application. En utilisant PIX sur toute une variété de configurations matérielles, les testeurs et les développeurs peuvent aider à réduire les appels au support technique liés aux performances des jeux.

## <a name="configuration-detection"></a>Détection de la configuration

Les fonctionnalités de l’appareil qui sont exposées par les pilotes ne sont pas toujours correctes. Une solution consiste à utiliser un système piloté par base de données pour la configuration des applications, comme le système présenté dans l’exemple de ConfigSystem, qui est inclus avec le kit de développement logiciel (SDK) DirectX. Un modèle de détection similaire au système dans l’exemple peut aider à identifier les fonctionnalités de l’appareil qui entravent les performances du jeu et, par conséquent, à réduire le nombre d’appels au support technique sur les performances.

## <a name="enable-full-compiler-warnings"></a>Activer les avertissements complets du compilateur

Il est recommandé de restaurer tous les avertissements du compilateur qui ont été désactivés par l' **\# Avertissement pragma** une fois qu’un projet est devenu stable. Les développeurs doivent essayer d’éliminer tous les avertissements avant de publier un produit. Même si un avertissement ne provoque pas un incident ou une erreur sur le système d’un développeur, il peut quand même poser un problème sur le système d’un utilisateur. Si un avertissement ne peut pas être éliminé, l’équipe des tests doit s’assurer que l’avertissement causera peu ou pas d’erreurs sur le système d’un utilisateur.

## <a name="microsoft-symbol-server"></a>Serveur de symboles Microsoft

microsoft fournit un serveur accessible sur Internet qui fournit des fichiers de symboles pour les systèmes d’exploitation microsoft Windows, ainsi que pour d’autres produits microsoft. les symboles sont également disponibles sur le serveur pour les versions bêta actuelles et les versions finales des produits Windows, ainsi que pour les correctifs et les service packs. Vous pouvez configurer le débogueur pour télécharger des symboles selon les besoins au cours d’une session de débogage, plutôt que de télécharger des fichiers de symboles séparément avant une session de débogage. Les symboles sont téléchargés vers un emplacement de répertoire que vous spécifiez et le débogueur les charge à partir de là.

Pour plus d’informations sur le serveur de symboles Microsoft, consultez [Outils et symboles de débogage : prise en main](https://www.microsoft.com/whdc/devtools/debugging/debugstart.mspx).

## <a name="windows-error-reporting"></a>Rapport d’erreurs Windows

Rapport d’erreurs Windows (WER) est un service fourni par Microsoft pour aider les développeurs à collecter des informations d’erreur à partir d’applications de manière unifiée et organisée. Bien qu’il soit complètement volontaire, les développeurs doivent tirer parti de ce service pour aider à déterminer les bogues qui se produisent le plus souvent. L’utilisation de WER peut faciliter le débogage des problèmes couramment signalés, ce qui permet d’éliminer les appels de support pour les bogues les plus répandus.

Pour plus d’informations sur le WER, consultez [analyse des vidages sur incident](./crash-dump-analysis.md).

## <a name="performance-tuning-tools"></a>Outils de réglage des performances

Les développeurs peuvent utiliser des analyseurs de performances pour ajuster les performances de leur jeu. outre PIX, il existe un certain nombre d’analyseurs de performances populaires pour Windows, tels que l' [analyseur de performances Intel VTune](https://software.intel.com/intel-vtune/) et l' [analyseur de performances AMD CodeAnalyst](https://developer.amd.com/cpu/CodeAnalyst/). Ces outils aident à identifier les goulots d’étranglement et à déterminer comment améliorer les performances globales d’une application. L’amélioration des goulots d’étranglement des performances avant la version permet de réduire les coûts de la publication.

## <a name="summary"></a>Résumé

Toute personne impliquée dans la conception, le développement et le test doivent réfléchir à la manière dont son travail aura un impact sur le coût de la publication d’un produit. En utilisant les outils et méthodes susmentionnés dans le processus de production, le volume d’appels de support peut être réduit. Cela augmentera ensuite les bénéfices en réduisant les coûts postérieurs au développement de jeux.

 

 