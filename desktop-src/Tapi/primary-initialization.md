---
description: Une application TAPI doit appeler une opération d’initialisation, qui invite une série d’actions à partir de l’interface TAPI et des fournisseurs de services qui configurent l’environnement de communication pour l’application.
ms.assetid: 10df0fb4-08d6-4ba0-85f7-108cc4e237c1
title: Initialisation principale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bcf37eecdee18861732dd27a4b134face9a17d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534030"
---
# <a name="primary-initialization"></a>Initialisation principale

Une application TAPI doit appeler une opération d’initialisation, qui invite une série d’actions à partir de l’interface TAPI et des fournisseurs de services qui configurent l’environnement de communication pour l’application.

-   L’initialisation est synchrone et n’est pas retournée tant que l’opération n’est pas terminée ou a échoué.
-   Si TAPISRV n’est pas déjà en cours d’exécution, TAPI le démarre.
-   L’interface TAPI configure une connexion au processus TAPISRV.
-   TAPISVR charge les fournisseurs de services spécifiés dans le registre et les invite à initialiser les appareils qu’ils prennent en charge.

**TAPI 2. x :** Les applications effectuent l’initialisation en appelant [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa).

**TAPI 3. x :** Les applications appellent [**ITTAPI :: Initialize**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-initialize).

 

 
