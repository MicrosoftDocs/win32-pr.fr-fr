---
description: utilisez ces instructions pour couvrir une installation Windows Installer complète par une signature numérique.
ms.assetid: e70eab94-4615-4a73-bccc-e16bd24551f6
title: Création d’une installation signée entièrement vérifiée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11d105b06e3f063d8cbeb1fac579beb12258b20062bf5cbae2cc6d08e9be6e4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066179"
---
# <a name="authoring-a-fully-verified-signed-installation"></a>Création d’une installation signée entièrement vérifiée

vous pouvez utiliser ces instructions pour couvrir une installation Windows Installer complète par une signature numérique.

les auteurs des installations de Windows Installer doivent respecter les conditions suivantes pour s’assurer que toutes les parties de l’installation sont couvertes par une signature numérique :

-   Utilisez des fichiers CAB internes ou des fichiers CAB externes signés et créez correctement la [table MsiDigitalSignature](msidigitalsignature-table.md) et la [table MsiDigitalCertificate](msidigitalcertificate-table.md).
-   Utilisez uniquement des actions personnalisées stockées dans le package ou installées avec le package.
-   Signez le package d’installation.
-   Incluez une [table MsiPatchCertificate](msipatchcertificate-table.md) dans le package. Pour activer la mise à [jour corrective du contrôle de compte d’utilisateur (UAC)](user-account-control--uac--patching.md), cette table doit contenir les informations utilisées pour identifier les certificats de signataire utilisés pour signer numériquement les correctifs. La mise à jour corrective du contrôle de compte d’utilisateur permet à l’auteur du package d’installation d’identifier les correctifs signés numériquement qui peuvent être appliqués ultérieurement par des utilisateurs non-administrateurs.

Pour obtenir un exemple illustrant comment créer une installation signée à l’aide d’Automation, consultez [création d’une installation signée entièrement vérifiée à l’aide d’Automation](authoring-a-fully-verified-signed-installation-using-automation.md).

 

 



