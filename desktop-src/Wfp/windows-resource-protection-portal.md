---
description: La protection des ressources empêche le remplacement des fichiers système et des dossiers et des clés de Registre essentiels pour le système d’exploitation. La modification des ressources protégées peut entraîner une défaillance du système ou de l’application.
ms.assetid: 27df9300-8bea-4748-9acd-2c1625093ece
title: Protection des ressources Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cff6c89e99b885256c7dd054a12c6a69795d794c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319862"
---
# <a name="windows-resource-protection"></a>Protection des ressources Windows

## <a name="purpose"></a>Objectif

Protection des ressources Windows (WRP) empêche le remplacement des fichiers système essentiels, des dossiers et des clés de Registre installés dans le cadre du système d’exploitation. Il est devenu disponible à partir de Windows Server 2008 et Windows Vista. Les applications ne doivent pas remplacer ces ressources, car elles sont utilisées par le système et d’autres applications. La protection de ces ressources empêche les défaillances de l’application et du système d’exploitation. WRP est le nouveau nom de la protection de fichiers Windows (WFP). WRP protège les clés de Registre et les dossiers, ainsi que les fichiers système essentiels.

## <a name="where-applicable"></a>Le cas échéant

Toutes les applications Windows et leurs programmes d’installation qui s’exécutent sur Windows Server 2008 ou Windows Vista, ainsi que sur les systèmes d’exploitation ultérieurs, doivent être conscients de WRP. Toutes les applications Windows qui s’exécutent sur Microsoft Windows Server 2003 ou Windows XP et leurs programmes d’installation doivent être conscientes de WFP.

## <a name="developer-audience"></a>Développeurs concernés

L’API WRP est conçue pour être utilisée par les programmeurs C/C++. L’API WRP a deux fonctions : [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) et [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected).

## <a name="run-time-requirements"></a>Conditions d’exécution

Les applications qui utilisent uniquement la fonction [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) nécessitent windows Server 2008, Windows Vista, windows Server 2003 ou Windows XP. Les applications qui utilisent la fonction [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected) nécessitent windows Server 2008 ou Windows Vista.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                     | Description                                 |
|-------------------------------------------------------------------------------------------|---------------------------------------------|
| [À propos de Protection des ressources Windows](about-windows-file-protection.md)<br/>         | Informations générales sur WRP.<br/>   |
| [Référence Protection des ressources Windows](windows-file-protection-reference.md)<br/> | Documentation de référence pour WRP.<br/> |



 

 

 




