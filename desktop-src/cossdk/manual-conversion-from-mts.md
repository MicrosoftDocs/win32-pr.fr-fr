---
description: Conversion manuelle à partir de MTS
ms.assetid: 7ecc64a8-783d-4238-8b63-8e9c76382723
title: Conversion manuelle à partir de MTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d384a6ca5f6afa2d0563249c78e1120349e28e053f1cad923a6ae2bdcdb8849
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070559"
---
# <a name="manual-conversion-from-mts"></a>Conversion manuelle à partir de MTS

vous souhaiterez peut-être isoler la conversion des packages MTS en applications COM+ afin qu’elles se trouvent en dehors du processus d’installation Windows. La procédure suivante offre une autre approche :

1.  Exportez les packages MTS à l’aide de la fonctionnalité d’exportation de package MTS 2,0 (ce qui génère un fichier de package MTS et une collection d’autres fichiers).
2.  supprimez les packages MTS et mettez à niveau Windows, ou effectuez une nouvelle installation de Windows.
3.  installez les fichiers de package MTS (. pak) sur un système Windows 2000 ou version ultérieure à l’aide de l’assistant installation d’applications de l’outil d’administration Services de composants. Vous devrez également réinitialiser l’identité « exécuter en tant que » de l’application dans le registre système sous **HKEY \_ local \_ machine \\ Software \\ classes \\ AppID \\ runas**.

> [!Note]  
> seule la procédure de conversion automatique (via le programme d’installation de Windows ou l’exécution de l’utilitaire MTSTOCOM) génère le fichier journal MTSTOCOM. Ce fichier n’est pas généré quand vous suivez la procédure de conversion manuelle.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Conversion automatique à partir de MTS](automatic-conversion-from-mts.md)
</dt> <dt>

[Résultats et problèmes de conversion COM+](com--conversion-results-and-issues.md)
</dt> <dt>

[Bibliothèque d’administration MTS](mts-administration-library.md)
</dt> </dl>

 

 



