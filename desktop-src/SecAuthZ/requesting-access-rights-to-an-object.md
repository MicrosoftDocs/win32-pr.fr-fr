---
description: Lorsque vous ouvrez un handle vers un objet, le handle retourné a une combinaison de droits d’accès à l’objet.
ms.assetid: 581de4ba-0f90-42d7-b7db-1324d42595e2
title: Demande de droits d’accès à un objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb2e13bd5f5e51ed194b60c6ab63d1eda8eddfa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193823"
---
# <a name="requesting-access-rights-to-an-object"></a>Demande de droits d’accès à un objet

Lorsque vous ouvrez un handle vers un objet, le handle retourné a une combinaison de droits d’accès à l’objet. Certaines fonctions, telles que [**CreateSemaphore,**](/windows/desktop/api/winbase/nf-winbase-createsemaphorea), ne nécessitent pas un ensemble spécifique de droits d’accès demandés. Ces fonctions essaient toujours d’ouvrir le descripteur pour un accès complet. D’autres fonctions, telles que [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) et [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess), vous permettent de spécifier le jeu de droits d’accès souhaité. Vous devez demander uniquement les droits d’accès dont vous avez besoin, plutôt que d’ouvrir un handle pour un accès complet. Cela empêche l’utilisation du descripteur de façon inattendue et augmente les chances que la demande d’accès aboutisse si le DACL de l’objet n’autorise que l’accès limité.

Utilisez les [droits d’accès génériques](generic-access-rights.md) pour spécifier le type d’accès nécessaire lors de l’ouverture d’un handle vers un objet. C’est généralement plus simple que de spécifier tous les droits standard et spécifiques correspondants. Vous pouvez également utiliser la \_ constante maximale autorisée pour demander à ce que l’objet soit ouvert avec tous les droits d’accès valides pour l’appelant.

> [!Note]  
> La \_ constante maximale autorisée ne peut pas être utilisée dans une entrée du contrôle d’accès.

 

Pour obtenir ou définir la liste SACL dans le [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly)d’un objet, demandez le droit accès à la [ \_ \_ sécurité du système Access](sacl-access-right.md) lors de l’ouverture d’un handle vers l’objet.

 

 
