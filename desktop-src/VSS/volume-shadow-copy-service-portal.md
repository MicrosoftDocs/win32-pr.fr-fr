---
description: Sauvegardez les volumes lorsque les applications sur un système continuent d’écrire sur les volumes. Réduisez le temps d’arrêt des applications en créant rapidement un instantané (cliché instantané) d’un volume qui duplique toutes les données. Effectuez une sauvegarde multivolume.
ms.assetid: 1eca1e3e-fc86-44b5-b3c4-bcee41bc5a43
title: Service VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2159d39f407f7ae5dbde454ab6cf3562307d892c
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443080"
---
# <a name="volume-shadow-copy-service"></a>Service VSS

## <a name="purpose"></a>Objectif

Le Service VSS (VSS) est un ensemble d’interfaces COM qui implémentent une infrastructure permettant d’effectuer des sauvegardes de volume alors que les applications sur un système continuent d’écrire sur les volumes.

Pour obtenir une présentation de VSS pour les administrateurs système, consultez [service VSS](/windows-server/storage/file-server/volume-shadow-copy-service) dans la bibliothèque TechNet.

## <a name="run-time-requirements"></a>Conditions d’exécution

VSS est pris en charge sur Microsoft Windows XP et versions ultérieures. Pour plus d’informations sur les exigences d’exécution d’un élément de programmation particulier, consultez la section Configuration requise de la documentation relative à cet élément.

Toutes les applications VSS 32 bits (demandeurs, fournisseurs et enregistreurs) doivent s’exécuter en tant qu’applications natives 32 bits ou 64 bits. Leur exécution sous WOW64 n’est pas prise en charge. Pour plus d’informations, consultez [configurations et restrictions prises en charge](usage-conventions.md).

**Windows Server 2003 et Windows XP :** L’exécution de demandeurs VSS 32 bits sous WOW64 est prise en charge, mais pas pour les sauvegardes de l’état du système. L’exécution des fournisseurs et des enregistreurs VSS 32 bits sous WOW64 n’est pas prise en charge. La prise en charge de l’exécution de demandeurs 32 bits sous WOW64 a été supprimée dans Windows Vista et les versions ultérieures.

> [!Note]  
> Un cliché instantané créé sur Windows Server 2003 R2 ou Windows Server 2003 ne peut pas être utilisé sur un ordinateur qui exécute Windows Server 2008 R2 ou Windows Server 2008. Un cliché instantané créé sur Windows Server 2008 R2 ou Windows Server 2008 ne peut pas être utilisé sur un ordinateur qui exécute Windows Server 2003. Toutefois, un cliché instantané créé sur Windows Server 2008 peut être utilisé sur un ordinateur qui exécute Windows Server 2008 R2, et vice versa.

 

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                          | Description                                                                                                                         |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [Vue d'ensemble](volume-shadow-copy-service-overview.md)<br/> | Décrit le modèle d’objet VSS, les stratégies de sauvegarde et de restauration, et comment créer des fournisseurs, des demandeurs et des enregistreurs VSS.<br/> |
| [Informations de référence](volume-shadow-copy-reference.md)<br/>       | Décrit les classes, les types de données, les énumérations, les fonctions, les interfaces et les structures VSS.<br/>                                  |



 

## <a name="additional-resources"></a>Ressources supplémentaires



|   Ressource                                 |   Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Vista et versions ultérieures            | VSS est disponible dans le kit de développement logiciel (SDK) Microsoft Windows. Vous pouvez installer le kit de développement logiciel (SDK) pour Windows 7 et Windows Server 2008 R2 à partir du [Centre de téléchargement Windows](https://www.microsoft.com/download/details.aspx?id=8279). Vous pouvez également télécharger la [version ISO](https://www.microsoft.com/download/details.aspx?id=8442) du kit de développement logiciel (SDK) à partir du centre de téléchargement Windows. Les versions précédentes du kit de développement logiciel (SDK) peuvent être téléchargées à partir de la [page de téléchargement SDK Windows](https://msdn.microsoft.com/windows/bb980924.aspx). |
| Windows Server 2003 et Windows XP | VSS est disponible dans le kit de développement logiciel (SDK) Service VSS 7,2, que vous pouvez télécharger à partir du [Centre de téléchargement Windows](https://www.microsoft.com/download/details.aspx?id=23490). Notez que les fichiers vssapi. lib 64 bits dans les répertoires du répertoire Win2003 \\ obj peuvent être utilisés pour les versions 64 bits de Windows Server 2003 et Windows XP.                                                                                                                                                                 |



 

 

 
