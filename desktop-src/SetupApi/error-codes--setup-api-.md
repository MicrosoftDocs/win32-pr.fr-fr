---
description: Les codes d’erreur suivants sont spécifiques à l’API d’installation.
ms.assetid: C4EB130F-2A83-4A14-BBA8-DB10225D0C0A
title: Codes d’erreur (API du programme d’installation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0c3955bd64f38946a59589259fc750892cfa9e84b3ef6e32ba2d9a5f6ca2244
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887338"
---
# <a name="error-codes-setup-api"></a>Codes d’erreur (API du programme d’installation)

Les codes d’erreur suivants sont spécifiques à l’API d’installation.



| Erreurs d’analyse INF              | Description                                                                                                         |
|---------------------------------|---------------------------------------------------------------------------------------------------------------------|
| ERREUR \_ de \_ nom de section attendue \_  | Un nom de section était attendu et introuvable.                                                                          |
| ERREUR \_ de \_ \_ ligne de nom de section erronée \_ | Le format du nom de la section n’est pas correct. (Par exemple, un nom qui ne se termine pas par un crochet droit ( \] ). |
| nom de section d’erreur \_ \_ \_ trop \_ long | Le nom de la section a dépassé la longueur maximale du nom de la \_ coupe Max \_ \_ .                                               |
| \_syntaxe générale de l’erreur \_          | La syntaxe générale est incorrecte.                                                                                    |



 



| Erreurs d’exécution INF         | Description                                                                                                                                                                                                                                    |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ERREUR \_ de \_ style INF incorrect \_   | Le fichier INF n’est pas du type spécifié dans l’appel de fonction. Par exemple, cette erreur peut être retournée par la fonction [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) si le fichier INF était destiné à une version antérieure de Windows. |
| \_section d' \_ erreur \_ introuvable | La section est introuvable dans le fichier INF.                                                                                                                                                                                                     |
| \_ligne d' \_ erreur \_ introuvable    | La ligne est introuvable dans la section INF.                                                                                                                                                                                                     |



 

 

 



