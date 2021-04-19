---
description: Chacune des sections suivantes traite d’une fonction exportée par Xenroll.dll pour gérer les messages d’échange d’informations personnelles (PFX).
ms.assetid: f7e6b3a6-eae4-49f8-a624-609742741560
title: Fonctions d’échange d’informations personnelles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dea1670e6017cd30ed8358d2670585727667068
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106540883"
---
# <a name="personal-information-exchange-functions"></a>Fonctions d’échange d’informations personnelles

Chacune des sections suivantes traite d’une fonction exportée par Xenroll.dll pour gérer les messages d’échange d’informations personnelles (PFX). Chaque section explique également comment utiliser CertEnroll.dll pour remplacer la fonction ou indique qu’il n’existe aucun mappage entre les deux bibliothèques.

## <a name="createfilepfxwstr"></a>createFilePFXWStr

La fonction [**createFilePFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createfilepfxwstr) dans Xenroll.dll enregistre une chaîne de certificats et une [*clé privée*](/windows/desktop/SecGloss/p-gly) dans un fichier à l’aide du format pfx.

La bibliothèque CertEnroll.dll n’implémente pas directement les fonctionnalités permettant de copier le message PFX dans un fichier. Toutefois, vous pouvez utiliser la méthode [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) sur l’interface [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) pour créer un message pfx encodé et écrire une fonction personnalisée pour enregistrer le message dans un fichier.

## <a name="createpfxwstr"></a>createPFXWStr

La fonction [**createPFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr) dans Xenroll.dll enregistre une chaîne de certificats et une clé privée dans une chaîne de format pfx.

Vous pouvez utiliser la méthode [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) sur l’interface [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) pour créer un message pfx encodé contenant la chaîne et la clé de certificat. Vous pouvez spécifier un mot de passe, des options d’exportation et un type de codage. Pour récupérer une chaîne qui est équivalente à celle retournée à partir de [**createPFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr), transmettez l' \_ indicateur binaire XCN crypto \_ String \_ dans le dans le paramètre *Encoding* de la méthode [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mappage de Xenroll.dll à CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
</dt> </dl>

 

 
