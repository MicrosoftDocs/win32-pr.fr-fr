---
description: La protection des ressources empêche le remplacement des fichiers système et des dossiers et des clés de Registre essentiels pour le système d’exploitation. La modification des ressources protégées peut entraîner une défaillance du système ou de l’application.
ms.assetid: 27df9300-8bea-4748-9acd-2c1625093ece
title: Windows Protection des ressources
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b00dabeadc662d3c13923d9d56e442388c53b7fa1e5740c651d689c3098bd049
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098579"
---
# <a name="windows-resource-protection"></a>Windows Protection des ressources

## <a name="purpose"></a>Objectif

Windows La protection des ressources (WRP) empêche le remplacement des fichiers système essentiels, des dossiers et des clés de Registre installés dans le cadre du système d’exploitation. il est devenu disponible à partir de Windows Server 2008 et Windows Vista. Les applications ne doivent pas remplacer ces ressources, car elles sont utilisées par le système et d’autres applications. La protection de ces ressources empêche les défaillances de l’application et du système d’exploitation. WRP est le nouveau nom de la protection de fichier Windows (WFP). WRP protège les clés de Registre et les dossiers, ainsi que les fichiers système essentiels.

## <a name="where-applicable"></a>Le cas échéant

toutes les applications basées sur Windows et leurs programmes d’installation qui s’exécutent sur Windows Server 2008 ou Windows Vista, et les systèmes d’exploitation ultérieurs, doivent être conscients de WRP. toutes les applications basées sur Windows qui s’exécutent sur Microsoft Windows Server 2003 ou Windows XP et leurs programmes d’installation doivent être conscientes de WFP.

## <a name="developer-audience"></a>Développeurs concernés

L’API WRP est conçue pour être utilisée par les programmeurs C/C++. L’API WRP a deux fonctions : [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) et [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected).

## <a name="run-time-requirements"></a>Conditions d’exécution

les Applications qui utilisent uniquement la fonction [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) nécessitent Windows server 2008, Windows Vista, Windows Server 2003 ou Windows XP. les Applications qui utilisent la fonction [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected) requièrent Windows Server 2008 ou Windows Vista.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                     | Description                                 |
|-------------------------------------------------------------------------------------------|---------------------------------------------|
| [à propos de Protection des ressources Windows](about-windows-file-protection.md)<br/>         | Informations générales sur WRP.<br/>   |
| [Windows Référence sur la protection des ressources](windows-file-protection-reference.md)<br/> | Documentation de référence pour WRP.<br/> |



 

 

 




