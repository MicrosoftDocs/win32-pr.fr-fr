---
description: Explique comment créer une demande de certificat et recevoir et stocker le certificat retourné dans un magasin de certificats.
ms.assetid: 4ca3d6cb-6ce7-4408-9258-6e40c8219dc0
title: Utilisation du contrôle d’inscription de certificats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d489edb7ed288ffc0b51d039c6c32df90631b833d491567729f075c1cee9cae0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117971756"
---
# <a name="using-certificate-enrollment-control"></a>Utilisation du contrôle d’inscription de certificats

Le contrôle d’inscription de certificats est un objet unique avec de nombreuses propriétés et plusieurs méthodes qui peuvent être utilisées pour déterminer comment le contrôle d’inscription de certificat traite les informations utilisateur, le type de certificat à demander, comment les clés doivent être générées, où le certificat doit être stocké et les processus associés. Il existe deux utilisations principales du contrôle d’inscription de certificats : pour créer une [*demande de certificat*](../secgloss/c-gly.md) (PKCS \# 10) et pour recevoir le certificat retourné et le stocker dans un [*magasin de certificats*](../secgloss/c-gly.md). Pour plus d’informations et pour connaître la syntaxe de création d’une instance de l’objet contrôle d’inscription de certificat, la définition de ses propriétés et l’utilisation de ses méthodes, consultez les rubriques suivantes.



| Information                                                                                                                                                                                           | Rubrique                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| Création d’une instance de l’objet de contrôle d’inscription de certificat dans différents langages de programmation                                                                                                  | [Création d’une instance de l’objet de contrôle d’inscription de certificat](creating-an-instance-of-the-certificate-enrollment-control-object.md) |
| Utilisation des propriétés de contrôle d’inscription de certificats dans différents langages de programmation                                                                                                                    | [Utilisation des propriétés du contrôle d’inscription de certificat](using-the-certificate-enrollment-control-properties.md)                             |
| La collecte des informations nécessaires et la soumission d’une [*demande de certificat*](../secgloss/c-gly.md) dans différents langages de programmation. | [Création de la demande de certificat](creating-the-certificate-request.md)                                                                   |
| Extraction et stockage du certificat terminé                                                                                                                                                      | [Réception du certificat retourné](receiving-the-returned-certificate.md)                                                               |
| Récupération d’informations à partir de valeurs de retour dans des langages différents                                                                                                                                      | [Valeurs de retour de méthode](method-return-values.md)                                                                                           |
| Vérification des erreurs                                                                                                                                                                                   | [Vérification des erreurs](error-checking.md)                                                                                                       |



 

 

 
