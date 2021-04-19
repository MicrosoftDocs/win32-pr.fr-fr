---
description: Inscrit un ordinateur dans une hiérarchie de certificats à l’aide d’un modèle, d’un nom d’affichage de certificat et de la description du certificat.
ms.assetid: d9e01767-f6e8-4fd6-a848-8d5acf57407e
title: enrollSimpleMachineCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8582bc73fdee7e8be6b2cff8d0aec81b84487307
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530580"
---
# <a name="enrollsimplemachinecert"></a>enrollSimpleMachineCert

L’exemple enrollSimpleMachineCert inscrit un ordinateur dans une hiérarchie de certificats à l’aide d’un modèle, d’un nom d’affichage de certificat et de la description du certificat.

## <a name="location"></a>Emplacement

Lorsque vous installez le kit de développement logiciel (SDK) Microsoft Windows, une version C++ de l’exemple est installée, par défaut, dans le dossier *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ x509 Certificate \\ \\ EnrollSimpleMachineCert VC. Une version VBScript est installée dans le dossier *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ x509 Certificate \\ EnrollSimpleMachineCert vbs \\ .

## <a name="discussion"></a>Discussions

Exemple enrollSimpleMachineCert :

1.  Traite les arguments de ligne de commande. La ligne de commande doit contenir le nom du modèle, un nom d’affichage du certificat et une description du certificat.
2.  Crée un objet [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) et l’initialise à l’aide du modèle spécifié sur la ligne de commande. La valeur ContextAdministratorForceMachine du premier paramètre spécifie que le certificat est demandé par un administrateur agissant pour le compte d’un ordinateur.
3.  Ajoute le nom complet et la description à l’objet d’inscription.
4.  Tente d’inscrire la demande de certificat et vérifie l’état du processus. La fonction checkEnrollStatus est définie dans enrollCommon. cpp.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des exemples inclus](using-the-included-samples.md)
</dt> </dl>

 

 



