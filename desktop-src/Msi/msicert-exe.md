---
description: Windows Le programme d’installation peut utiliser des signatures numériques pour détecter les ressources endommagées.
ms.assetid: fc982813-583b-4fcd-88d8-9de227994e7b
title: Msicert.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ede88930cdb6cc616d8c39fb400f0c67c31eecd01d6d1a7d1832421cb394bcc4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119534542"
---
# <a name="msicertexe"></a>Msicert.exe

Windows Le programme d’installation peut utiliser des signatures numériques pour détecter les ressources endommagées. Un certificat de signataire peut être comparé au certificat de signataire d’une ressource externe qui doit être installée par le package. pour plus d’informations, consultez [Signatures numériques et Windows Installer](digital-signatures-and-windows-installer.md).

MsiCert.exe est un utilitaire de ligne de commande qui peut être utilisé pour remplir la table [MsiDigitalSignature](msidigitalsignature-table.md) et la [table MsiDigitalCertificate](msidigitalcertificate-table.md) avec les informations de signature numérique d’un fichier CAB externe. Le fichier cab doit être signé numériquement et listé dans la [table des médias](media-table.md). MsiCert.exe utilise les informations de certificat du signataire de l’armoire signée numériquement et crée et ajoute les tables MsiDigitalSignature et MsiDigitalCertificate à la base de données si elles n’existent pas déjà.

## <a name="syntax"></a>Syntaxe

**msicert-d** *{base de données}* **-m** *{entrée de support}* **-c** *{Cabinet}* **\[ -h \]**

## <a name="command-line-options"></a>Options de la ligne de commande

Les options de ligne de commande ne respectent pas la casse et les séparateurs de barres obliques peuvent être utilisés à la place d’un tiret.



| Option | Paramètre        | Description                                                                                             |
|--------|------------------|---------------------------------------------------------------------------------------------------------|
| -d     | <database> | La base de données (fichier .msi) en cours de mise à jour.                                                         |
| -M     | <media Id> | Entrée dans le champ depatinage de la [table Media](media-table.md) de l’enregistrement du fichier CAB. |
| -c     | <cabinet>  | Chemin d’accès au fichier CAB signé numériquement.                                                          |
| -H     |                  | Incluez le hachage de la signature numérique. Cette étape est facultative.                                            |



 

cet outil est disponible uniquement dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Outils de développement du programme d’installation](windows-installer-development-tools.md)
</dt> <dt>

[Versions, outils et redistribuables publiés](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



