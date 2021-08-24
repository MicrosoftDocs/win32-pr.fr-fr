---
description: Cette rubrique décrit les alternatives à l’utilisation de l’API NTFS transactionnelle (TxF) dans les scénarios d’utilisation courants.
ms.assetid: 9ee26e7e-990e-4cd3-8180-f0fcaac2b752
title: Alternatives à l’utilisation de NTFS transactionnel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ab924c5ee4204180b891b3aad13a5809fa07671ad0e18d6ddc9ce353122ac80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765969"
---
# <a name="alternatives-to-using-transactional-ntfs"></a>Alternatives à l’utilisation de NTFS transactionnel

-   [Résumé](#abstract)
-   [Introduction](#introduction)
-   [Alternatives à TxF par scénario](#alternatives-to-txf-by-scenario)
-   [Applications mettant à jour un seul fichier avec des données de type « document »](#applications-updating-a-single-file-with-document-like-data)
-   [Applications effectuant des mises à jour de plusieurs fichiers et/ou de la ruche du Registre](#applications-performing-updates-to-multiple-files-andor-to-the-registry-hive)
-   [Applications gérant un ensemble de données structurées](#applications-managing-a-set-of-structured-data)
-   [Applications avec des Transactions impliquant des fichiers situés sur un volume NTFS local et des Tables dans une base de données SQL externe](#applications-with-transactions-involving-files-on-a-local-ntfs-volume-and-tables-in-an-external-sql-database)
-   [Fermeture & action recommandée](/windows)

## <a name="abstract"></a>Résumé

Microsoft recommande vivement aux développeurs d’examiner l’utilisation des alternatives décrites (ou, dans certains cas, d’examiner d’autres solutions) au lieu d’adopter une plateforme d’API qui n’est peut-être pas disponible dans les futures versions de Windows.

## <a name="introduction"></a>Introduction

TxF a été introduit avec Windows Vista comme un moyen d’introduire des transactions de fichier atomiques pour Windows. il permet à Windows aux développeurs d’avoir une atomicité transactionnelle pour les opérations de fichier dans les transactions avec un seul fichier, dans les transactions impliquant plusieurs fichiers et dans les transactions qui couvrent plusieurs sources, telles que le registre (via TxR) et les bases de données (telles que SQL). tandis que TxF est un ensemble puissant d’api, il a été très limité en ce qui concerne les développeurs dans cette plateforme d’API, car Windows Vista est principalement dû à sa complexité et aux différentes nuances que les développeurs doivent prendre en compte dans le cadre du développement d’applications. par conséquent, Microsoft envisage d’utiliser les api TxF dans une future version de Windows pour concentrer les efforts de développement et de maintenance sur d’autres fonctionnalités et api qui ont plus de valeur pour une plus grande majorité des clients. La section suivante décrit des exemples de méthodes alternatives pour obtenir des résultats similaires à ceux de TxF pour plusieurs types de scénarios d’application.

## <a name="alternatives-to-txf-by-scenario"></a>Alternatives à TxF par scénario

Avec les limitations décrites ci-dessus, les développeurs doivent examiner les alternatives à TxF pour couvrir les scénarios d’application qui ne sont pas satisfaits par TxF. Voici quelques suggestions d’alternatives aux utilisations courantes de TxF que les développeurs peuvent prendre en compte. Notez que cette liste n’est ni exhaustive, ni complète.

## <a name="applications-updating-a-single-file-with-document-like-data"></a>Applications mettant à jour un seul fichier avec des données de type « document »

De nombreuses applications qui traitent des données de type « document » tendent à charger l’intégralité du document dans la mémoire, à les utiliser, puis à les réécrire pour enregistrer les modifications. L’atomicité nécessaire ici est que les modifications sont complètement appliquées ou non appliquées, car un état incohérent rendrait le fichier endommagé. Une approche courante consiste à écrire le document dans un nouveau fichier, puis à remplacer le fichier d’origine par le nouveau. Pour ce faire, vous pouvez utiliser l’API [**ReplaceFile**](/windows/desktop/api/WinBase/nf-winbase-replacefilea) .

## <a name="applications-performing-updates-to-multiple-files-andor-to-the-registry-hive"></a>Applications effectuant des mises à jour de plusieurs fichiers et/ou de la ruche du Registre

De nombreuses applications doivent effectuer atomiquement une mise à jour d’un ensemble de fichiers et du Registre. ce scénario est le plus souvent réalisé par le biais d’une application de programme d’installation, par exemple Windows Installer. pour plus d’informations sur Windows Installer, consultez [Windows Installer](/windows/desktop/Msi/windows-installer-portal).

## <a name="applications-managing-a-set-of-structured-data"></a>Applications gérant un ensemble de données structurées

De nombreuses applications gèrent un ensemble de structures de données propriétaires de types variables comme un moyen de stocker des données. Un défi majeur pour ces applications est le processus de maintien de l’intégrité des pointeurs/références internes si une défaillance se produit pendant une opération de mise à jour. La création du mécanisme pour cela est en fait un « problème difficile » et, par conséquent, la plupart des applications s’appuient sur un véritable serveur de base de données pour gérer leur jeu de données.

Voici deux suggestions pour vous aider à gérer les données structurées :

-   Microsoft fournit la boîte de réception ese (Extensible Stockage Engine) dans Windows pour permettre aux applications d’effectuer des opérations de mise à jour et de récupération des données transactionnelles. pour plus d’informations sur le moteur ese (Extensible Stockage Engine), consultez <https://msdn.microsoft.com/library/gg269259.aspx> .
-   Pour les applications qui requièrent un fournisseur de base de données plus puissant, robuste et évolutif, il est recommandé que les clients envisagent d’utiliser la fonctionnalité FileStream disponible avec Microsoft SQL Server. pour plus d’informations sur SQL filestreams, consultez <https://technet.microsoft.com/library/bb933993.aspx> .

## <a name="applications-with-transactions-involving-files-on-a-local-ntfs-volume-and-tables-in-an-external-sql-database"></a>Applications avec des Transactions impliquant des fichiers situés sur un volume NTFS local et des Tables dans une base de données SQL externe

Il existe des classes d’applications qui ont des besoins de jeu de données volumineux, ou qui doivent avoir une atomicité transactionnelle dans une opération impliquant une base de données externe et un stockage local. pour ce scénario, il est fortement recommandé que les développeurs envisagent d’utiliser SQL filestreams pour effectuer des opérations de fichier transactionnel. pour plus d’informations sur SQL filestreams, consultez <https://technet.microsoft.com/library/bb933993.aspx> .

## <a name="closing--recommended-action"></a>Fermeture & action recommandée

TxF est un ensemble complexe et en nuances d’API qui ne sont pas couramment utilisés par des applications tierces. avec la possibilité que ces api ne soient pas disponibles dans les versions ultérieures de Windows, et le fait qu’il existe des moyens plus simples d’effectuer un grand nombre des scénarios pour lesquels txf a été développé, Microsoft recommande vivement aux développeurs d’examiner ces autres moyens au lieu de créer une dépendance sur TxF dans leurs applications.

 

 
