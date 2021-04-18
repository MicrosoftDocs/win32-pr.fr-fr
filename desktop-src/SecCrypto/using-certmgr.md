---
description: Utilisez CertMgr pour afficher des certificats, des listes de révocation de certificats et des listes CTL à partir d’un fichier ou d’un magasin de certificats, copier des certificats dans un magasin de certificats, supprimer des certificats d’un magasin de certificats et enregistrer des certificats dans des fichiers.
ms.assetid: cc2424bf-e7ea-4484-9934-3aba02b63492
title: Utilisation de CertMgr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef7e22862184f87e1f070a4683d313cb1457e7d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527200"
---
# <a name="using-certmgr"></a>Utilisation de CertMgr

Vous pouvez utiliser [certmgr](certmgr.md) [*pour afficher des certificats,*](../secgloss/c-gly.md)des [*listes de révocation*](../secgloss/c-gly.md) de certificats (CRL) et des listes de certificats de [*confiance*](../secgloss/c-gly.md) (CTL) à partir d’un fichier ou d’un magasin de certificats, copier des certificats dans un [*magasin de certificats*](../secgloss/c-gly.md), supprimer des certificats d’un magasin de certificats et enregistrer des certificats dans des fichiers.

Lorsque [certmgr](certmgr.md) est utilisé sans options, un Assistant certmgr s’affiche pour guider l’utilisateur tout au long de l’opération.

Le fichier doit être de l’un des types suivants :

-   Un fichier de certificat, de liste de révocation de certificats ou de liste de révocation de certificats encodé (peut être encodé en base 64)
-   Un \# fichier PKCS 7
-   Un fichier SPC
-   Un document signé
-   StoreFile sérialisé

Les exemples suivants utilisent des commandes [certmgr](certmgr.md) pour effectuer des tâches de certificat courantes.

-   Affichez les certificats, les listes de révocation de certificats et les listes CTL de *MyFile. ext*.

    **certmgr** *MyFile. ext*

-   Affichez les certificats, les listes de révocation de certificats et les listes CTL à partir du magasin mon système.

    **certmgr-s My**

-   Copiez tous les certificats, listes de révocation de certificats et listes de certificats de confiance dans un fichier nommé *MyFile. ext* dans un nouveau fichier nommé *NewFile. ext*.

    **certmgr-Add-All-c** *MyFile. ext* *NewFile. ext*

-   Copiez tous les certificats, listes de révocation de certificats et listes de certificats de confiance du magasin MY System dans un fichier appelé *NewMyFile. ext*.

    **certmgr-Add-All-c-s My** *NewMyFile. ext*

-   Copiez un certificat avec le nom commun *myCert* dans le magasin My System dans un fichier appelé *newCert. cer*.

    **certmgr-Add-c-n** *myCert* **-s My** *newCert. cer*

-   Supprimez tous les certificats du magasin mon système.

    **certmgr-del-All-c-s My**

-   Supprimez toutes les listes CTL du magasin MY System et enregistrez le magasin qui en résulte dans un fichier appelé *NewStore. Str*.

    **certmgr-del-All-CTL-s My** *NewStore. Str*

-   Enregistrez dans un fichier nommé *newCert. cer*, un certificat qui est un certificat encodé [*X. 509*](../secgloss/x-gly.md) , dont le nom commun est *myCert*, et qui se trouve dans le magasin de certificats racine.

    **certmgr-put-c-n** *myCert* **-s racine** *newCert. cer*

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[CertMgr](certmgr.md)
</dt> </dl>

 

 
