---
description: Cert2SPC
ms.assetid: d05df388-c19d-47a5-9ede-11cf06c29fc8
title: Cert2SPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1680f8fe426c2e3a62cac0674928a1520b402357
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106539802"
---
# <a name="cert2spc"></a>Cert2SPC

L’outil Cert2SPC crée un certificat SPC (test [*Software Publisher Certificate*](../secgloss/s-gly.md) ) à l’aide de [*certificats*](../secgloss/c-gly.md) [*X. 509*](../secgloss/x-gly.md) existants. Cert2SPC peut encapsuler plusieurs certificats X. 509 dans un objet de données signées [*PKCS \# 7*](../secgloss/p-gly.md) . L’outil est installé dans le \\ dossier bin du chemin d’installation du kit de développement logiciel (SDK) Microsoft Windows.

Cert2SPC est disponible dans le cadre de la SDK Windows, que vous pouvez télécharger à partir de <https://go.microsoft.com/fwlink/p/?linkid=84091> .

> [!Note]
> Cet outil est destiné à des fins de test uniquement. Un SPC valide est obtenu à partir d’une [*autorité de certification*](../secgloss/c-gly.md).


**Cert2spc** *Cert1. cer Cert2. cer* ... *Sortie. spc*

 



|                         |                                                                                                                                    |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| *Cert1. cer Cert2. cer* ... | Noms des certificats X. 509 à inclure dans le SPC. Chaque nom de certificat se termine par l’extension. cer.                         |
| *Sortie. spc*            | Nom de l' \# objet PKCS 7 qui contient les certificats X. 509 à créer. Le nom du fichier de sortie se termine par l’extension. spc. |



 

 

 
