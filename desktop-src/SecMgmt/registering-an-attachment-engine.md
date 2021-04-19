---
description: Avant que le moteur de configuration de la sécurité puisse appeler votre moteur d’attachement pour traiter des tâches spécifiques au service, vous devez installer votre moteur de pièces jointes et l’inscrire auprès du moteur de configuration de sécurité.
ms.assetid: f7376a79-97cd-4607-9e1b-5b8c7cd76a32
title: Inscription d’un moteur de pièce jointe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f50827fe27e86328e7e914bfc98740fa5e15060
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514162"
---
# <a name="registering-an-attachment-engine"></a>Inscription d’un moteur de pièce jointe

Avant que le moteur de configuration de la sécurité puisse appeler votre moteur d’attachement pour traiter des tâches spécifiques au service, vous devez installer votre moteur de pièces jointes et l’inscrire auprès du moteur de configuration de sécurité.

**Pour installer et inscrire la DLL du moteur de pièces jointes**

1.  Copiez la DLL du moteur de pièces jointes dans un répertoire sur le système. Le répertoire préféré est% windir% \\ secedit \\ Attachments. Si ce répertoire n’existe pas, vous devez le créer.
2.  Créez une clé de Registre sous le nœud suivant. Le nom du *service* est le nom inscrit pour la pièce jointe et doit être le même nom de service que celui utilisé dans le gestionnaire de contrôle des services, un module qui gère l’arrêt et le démarrage des services. Le nom doit également être unique, de sorte qu’il n’est pas en conflit avec les noms des autres pièces jointes.

    ```
    HKEY_LOCAL_MACHINE
       Microsoft
          Windows NT
             CurrentVersion
                SeCEdit
                   Service
                      service name
    ```

3.  Créez la valeur de chaîne suivante dans la nouvelle clé de registre. le *chemin d’accès du moteur des pièces jointes* est le chemin d’accès complet au module du moteur d’attachement.<dl> <dd>**ServiceAttachmentPath**  =  *chemin du moteur des pièces jointes*<dl> <dt>

Type de données
</dt> <dd>REG_SZ</dd> </dl> </dd> </dl>

 

 



