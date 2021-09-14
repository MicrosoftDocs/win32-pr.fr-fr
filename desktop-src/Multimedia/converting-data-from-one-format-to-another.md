---
title: Conversion de données d’un format à un autre
description: Conversion de données d’un format à un autre
ms.assetid: df995b7d-ac45-4964-a1b0-efd079c0c010
keywords:
- Gestionnaire de compression audio (ACM), conversion de données
- ACM (gestionnaire de compression audio), conversion de données
- Exemples ACM, conversion de données
- convertir des données
- acmStreamOpen fonction)
- acmStreamSize fonction)
- acmStreamPrepareHeader fonction)
- acmStreamConvert fonction)
- acmStreamUnprepareHeader fonction)
- acmStreamClose fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9645342aa9f19b2c31de77dc9d1031122ed0b2ac
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127233807"
---
# <a name="converting-data-from-one-format-to-another"></a>Conversion de données d’un format à un autre

L’ACM utilise des fonctions de flux pour prendre en charge la conversion de format de données. Les convertisseurs dans l’ACM modifient le format, mais pas le type de données. Par exemple, un module de conversion peut remplacer les données 44-kHz, 16 bits par des données 8 bits 44-kHz.

Les fonctions ACM suivantes prennent en charge la conversion de format de données. Ils sont répertoriés dans l’ordre dans lequel vous les utilisez généralement.

-   La fonction [**acmStreamOpen**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen) ouvre un flux de conversion.
-   La fonction [**acmStreamSize**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize) calcule la taille appropriée de la mémoire tampon source ou de destination.
-   La fonction [**acmStreamPrepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader) prépare les mémoires tampons sources et de destination à utiliser dans une conversion.
-   La fonction [**acmStreamConvert**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert) convertit les données d’une mémoire tampon source au format de destination, en écrivant les données converties dans la mémoire tampon de destination.
-   La fonction [**acmStreamUnprepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader) nettoie les mémoires tampons sources et de destination préparées par **acmStreamPrepareHeader**. Vous devez appeler cette fonction avant de libérer les mémoires tampons sources et de destination.
-   La fonction [**acmStreamClose**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose) ferme un flux de conversion.

Lors de la conversion de données, identifiez d’abord le format source, puis choisissez le format de destination. Pour ce faire, la méthode la plus simple consiste à utiliser la fonction [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) , qui affiche une boîte de dialogue de sélection de format et retourne le choix de format de l’utilisateur.

Lorsque vous connaissez les formats source et de destination, vous pouvez utiliser [**acmStreamOpen**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen) pour ouvrir un flux de conversion. Vous pouvez ensuite utiliser la fonction [**acmStreamSize**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize) pour déterminer les tailles de mémoire tampon appropriées.

L’étape suivante consiste à préparer les mémoires tampons à utiliser dans la conversion à l’aide de [**acmStreamPrepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader).

Pour effectuer la conversion, utilisez [**acmStreamConvert**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert) jusqu’à ce que toutes les mémoires tampons aient été traitées. Une fois la conversion terminée, utilisez [**acmStreamUnprepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader) pour nettoyer les tampons, puis utilisez [**acmStreamClose**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose) pour fermer le flux de conversion.

 

 




