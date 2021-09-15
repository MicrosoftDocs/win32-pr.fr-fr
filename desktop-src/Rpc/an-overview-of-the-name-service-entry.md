---
title: Vue d’ensemble de l’entrée Service Name
description: L’entrée service de nom se compose de trois sections distinctes.
ms.assetid: 3059a9a9-174d-4d04-8565-e4558f17f465
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efc3855f586582b013bc47b11eb058ae461014f4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127238206"
---
# <a name="an-overview-of-the-name-service-entry"></a>Vue d’ensemble de l’entrée Service Name

L’entrée service de nom se compose de trois sections distinctes. La première section concerne les interfaces (UUID + version), la deuxième section contient les UUID d’objet, et la troisième section concerne les handles de liaison. Vous devez fournir un nom pour l’entrée qui servira de méthode pour l’identifier.

Lors de l’appel de [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta), le serveur spécifie le nom de l’entrée dans laquelle placer les informations exportées. Cette interface récemment exportée est ensuite ajoutée à la section interface de l’entrée Service Name. Toutes les interfaces déjà présentes dans l’entrée de service de nom sont également conservées. Ce même processus est suivi pour les UUID d’objet et les handles de liaison.

Le client appelle [**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina) (ou [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)) pour rechercher un handle de liaison approprié. Le nom de l’entrée, le descripteur d’interface et l’UUID de l’objet sont extraits. Celles-ci restreignent les entrées à partir desquelles les handles de liaison sont retournés. Si une entrée correspond aux critères de recherche, tous les descripteurs de liaison de cette entrée sont retournés à partir de [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext).

 

 




