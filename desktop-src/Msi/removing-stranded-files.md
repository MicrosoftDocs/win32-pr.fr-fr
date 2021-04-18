---
description: Liste des raisons possibles pour lesquelles une désinstallation de Windows Installer n’a pas pu supprimer tous les fichiers d’une application.
ms.assetid: 0a856f0f-a829-478e-a83b-dade7b05b4f2
title: Suppression des fichiers bloqués
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d5eeceb45c2139d146c32bdf9917e41885688df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519993"
---
# <a name="removing-stranded-files"></a>Suppression des fichiers bloqués

Si un fichier qui aurait dû être supprimé de l’ordinateur de l’utilisateur reste installé après l’exécution d’une désinstallation, il se peut que le programme d’installation ne supprime pas le composant contenant le fichier pour une ou plusieurs des raisons suivantes :

-   Le bit msidbComponentAttributesPermanent a été défini pour le composant dans la colonne attributs de la [table des composants](component-table.md).
-   Aucune valeur n’a été entrée pour le composant dans la colonne ComponentId de la table des composants.
-   Le composant est utilisé par une autre application ou fonctionnalité qui est encore installée.
-   Une condition est spécifiée dans la table de [conditions](condition-table.md) qui active une fonctionnalité lors de l’installation et désactive la fonctionnalité lors de la désinstallation.
-   Le fichier de clé du composant a un nombre de références antérieur sous **HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **SharedDLLs**.
-   Le composant est installé dans le dossier système et tous les fichiers du composant ont un nombre de références antérieur sous **HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **SharedDLLs**.
-   Le Windows Installer ne supprime pas les fichiers ou clés de Registre protégés par [protection des ressources Windows](../wfp/windows-resource-protection-portal.md) (WRP). Pour plus d’informations, consultez [utilisation de Windows Installer et protection des ressources Windows](windows-resource-protection-on-windows-vista.md). Sur Windows Server 2003, Windows XP et Windows 2000, le programme d’installation ne supprime pas les fichiers protégés par la protection de fichiers Windows (WFP). Si la clé de registre ou le fichier du chemin d’accès de la clé d’un composant est protégé par WFP ou WRP, le programme d’installation ne supprime pas le composant.
    > [!Note]  
    > Étant donné que Windows Installer n’installe, ne met pas à jour ou ne supprime aucune ressource protégée par WRP, vous ne devez pas inclure de ressources protégées dans un package d’installation. Au lieu de cela, utilisez uniquement les [mécanismes de remplacement de ressources pris en charge](../wfp/supported-file-replacement-mechanisms.md) décrits dans la section [protection des ressources Windows](../wfp/windows-resource-protection-portal.md) .

     

 

 
