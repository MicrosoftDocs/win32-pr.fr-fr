---
description: Windows Les fonctions de programme d’installation qui retournent des données dans un emplacement fourni par l’utilisateur ne doivent pas être appelées avec NULL comme valeur du pointeur.
ms.assetid: f566c4a4-b90c-4d73-9d7f-f5b836630636
title: passage de la valeur null aux fonctions Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc6964716479d7e64cc9aa70d7e49acc8fe78dd3343298826e011f6d72b4df1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118627662"
---
# <a name="passing-null-as-the-argument-of-windows-installer-functions"></a>passage de null comme Argument des fonctions Windows Installer

Windows Les fonctions de programme d’installation qui retournent des données dans un emplacement fourni par l’utilisateur ne doivent pas être appelées avec NULL comme valeur du pointeur. Ces fonctions retournent une chaîne ou retournent des données sous forme de pointeurs entiers, mais retournent des valeurs incohérentes lors du passage de NULL comme valeur de l’argument de sortie.

Ne transmettez pas NULL comme valeur de l’argument de sortie pour l’une des fonctions suivantes :

[**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya)

[**MsiRecordGetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa)

[**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)

[**MsiGetSourcePath**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsourcepatha)

[**MsiGetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha)

[**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)

[**MsiViewGetError**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora)

[**MsiSummaryInfoGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya)

[**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona)

[**MsiGetFeatureCost**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)

[**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)

[**MsiGetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)

[**MsiGetFeatureCost**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)

[**MsiGetFeatureValidStates**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa)

 

 



