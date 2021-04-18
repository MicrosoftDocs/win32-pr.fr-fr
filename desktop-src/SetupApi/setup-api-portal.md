---
description: Installe des pilotes de périphérique à partir de programmes avec un script de configuration et des fichiers INF. Écrivez un programme d’installation pour la configuration des appareils et l’installation du pilote. Cette API n’est plus recommandée dans le cadre de l’installation d’applications logicielles.
ms.assetid: 96a9e472-9b92-4976-9379-dc0c96524963
title: API d’installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6101c2673e72095d0cf4ebe59c1cece83449d647
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519971"
---
# <a name="setup-api"></a>API d’installation

## <a name="purpose"></a>Objectif

L’API d’installation fournit un ensemble de fonctions que l’application de configuration appelle pour effectuer des opérations d’installation.

## <a name="where-applicable"></a>Le cas échéant

Ces fonctions de configuration sont disponibles pour le développement d’une application d’installation. L’API d’installation ne doit plus être utilisée pour installer des applications. Utilisez plutôt le [Windows Installer](/windows/desktop/Msi/windows-installer-portal)pour développer des programmes d’installation d’application. L’API d’installation continue à être utilisée pour installer les pilotes de périphérique.

L’API d’installation est destinée au développement d’applications de style bureau.

## <a name="developer-audience"></a>Développeurs concernés

Un développeur peut utiliser l’API d’installation si son application d’installation requiert les fonctionnalités suivantes :

-   Mise en file d’attente de fichiers.
-   Installation des fichiers.
-   Gestion des erreurs d’installation et demande de support.
-   Mise à jour des entrées de registre.
-   Journalisation des fichiers au fur et à mesure de leur installation.
-   Stockage des chemins sources les plus récemment utilisés.

## <a name="run-time-requirements"></a>Conditions d’exécution

Pour plus d’informations sur les systèmes d’exploitation requis pour utiliser une fonction particulière, consultez la section Configuration requise de la documentation relative à la fonction.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                 | Description                                                                                 |
|---------------------------------------|---------------------------------------------------------------------------------------------|
| [Vue d'ensemble](overview.md)<br/>   | Informations générales sur l’API d’installation.<br/>                                             |
| [Référence](reference.md)<br/> | Documentation des types de données, des structures, des fonctions et des notifications de l’API d’installation.<br/> |



 

 

