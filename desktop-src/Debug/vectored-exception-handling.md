---
description: Les gestionnaires d’exceptions vectorisées sont une extension de la gestion structurée des exceptions.
ms.assetid: e4cf8a88-1bdf-4666-8653-fe2e86c4d8ef
title: Gestion des exceptions vectorisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 011310b46ce8912e03b6481e9b12b986174a3ef0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861126"
---
# <a name="vectored-exception-handling"></a>Gestion des exceptions vectorisées

Les gestionnaires d’exceptions vectorisées sont une extension de la gestion structurée des exceptions. Une application peut enregistrer une fonction pour surveiller ou gérer toutes les exceptions pour l’application. Les gestionnaires vectorisés ne sont pas basés sur des trames. par conséquent, vous pouvez ajouter un gestionnaire qui sera appelé, quel que soit l’endroit où vous vous trouvez dans un frame d’appel. Les gestionnaires vectorisés sont appelés dans l’ordre dans lequel ils ont été ajoutés, après que le débogueur ait effectué une notification de première chance, mais avant que le système ne commence à dérouler la pile.

Pour ajouter un gestionnaire de continuation vectorisé, utilisez la fonction [**AddVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredcontinuehandler) . Pour supprimer ce gestionnaire, utilisez la fonction [**RemoveVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredcontinuehandler) .

Pour ajouter un gestionnaire d’exceptions vectorisées, utilisez la fonction [**AddVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredexceptionhandler) . Pour supprimer ce gestionnaire, utilisez la fonction [**RemoveVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredexceptionhandler) .

 

 
