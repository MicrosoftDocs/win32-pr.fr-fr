---
description: Plusieurs fonctions fournissent des services pour la gestion de l’état d’un magasin de certificats.
ms.assetid: bae3d693-31b3-4c1d-9a8f-0dafa8bb6897
title: Gestion de l’état d’un magasin de certificats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75cbbb41691b66abfa2d49d669b13ec7fd438bd4ae503bf944d9e4923f647f29
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119425669"
---
# <a name="managing-a-certificate-store-state"></a>Gestion de l’état d’un magasin de certificats

Plusieurs fonctions fournissent des services pour la gestion de l' [*État*](../secgloss/s-gly.md)d’un [*magasin de certificats*](../secgloss/c-gly.md) .

Pour accéder aux certificats, le magasin de certificats dans lequel ils sont stockés doit être ouvert par un appel à [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) ou [**CertOpenSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopensystemstorea).

En général, un magasin de certificats est ouvert dans la mémoire mise en cache. Il peut s’agir d’un nouveau magasin ou son contenu peut être chargé à partir du registre local, du Registre sur un ordinateur distant, d’un fichier disque, d’un \# message PKCS 7 ou d’une autre source.

Les fonctions de magasin de certificats CryptoAPI permettent également à un magasin de conserver des certificats en dehors de la mémoire mise en cache dans, par exemple, une base de données externe de certificats, telle que celle fournie par la base de données du serveur de certificats Microsoft.

L’un des paramètres de la fonction [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) , *lpszStoreProvider,* détermine le type de magasin ouvert et le fournisseur utilisé pour ouvrir ce magasin. Pour obtenir des exemples d’ouverture de magasins de certificats à l’aide de différents fournisseurs, consultez l' [exemple de code C pour l’ouverture de magasins de certificats](example-c-code-for-opening-certificate-stores.md).

[**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) ferme un magasin de certificats. Lors de la fermeture d’un magasin de certificats, le [*nombre de références*](../secgloss/r-gly.md) de chacun des contextes de certificat de ce magasin est réduit d’une unité. La mémoire est libérée pour les certificats dont le décompte de références atteint zéro.

La définition \_ de \_ \_ \_ l’indicateur de force du magasin de fermeture de certificat avec [**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) ferme le magasin de certificats et libère de la mémoire pour tous ses contextes de certificats, quel que soit le nombre de références. Dans certains cas, comme dans les programmes multithread, cela ne peut pas être souhaitable. Si \_ \_ \_ l’indicateur de validation du magasin de fermeture du certificat \_ est défini, le magasin est fermé, mais une valeur d’avertissement est retournée par la fonction si la mémoire est toujours allouée pour les certificats dont le nombre de références n’a pas été réduit à zéro. Si le nombre de références d’un certificat est supérieur à zéro, un doublon de ce contexte de certificat n’a pas été libéré. Utilisez [**CertFreeCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext), [**CertFreeCRLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecrlcontext)et [**CertFreeCTLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreectlcontext) pour libérer tous les certificats laissés ouverts.

> [!Note]
> Un [*contexte de certificat*](../secgloss/c-gly.md) est une structure de [**type CERT \_ Context**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) qui a, entre autres membres, un pointeur vers l' [*objet blob de certificat*](../secgloss/c-gly.md) encodé et un pointeur vers une structure d' [**\_ informations**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) de certificat. La structure des **\_ informations** de certificat contient les données de certificat les plus significatives. Pour plus d’informations sur les structures de contexte [*Certificate*](../secgloss/c-gly.md), [*liste de révocation de certificats*](../secgloss/c-gly.md) et liste de certificats de [*confiance*](../secgloss/c-gly.md) (CTL), consultez [encodage et décodage d’un contexte de certificat](encoding-and-decoding-a-certificate-context.md).
> 
> Chaque contexte de certificat contient également un nombre de [*références*](../secgloss/r-gly.md) indiquant le nombre de copies de l’adresse du contexte qui ont été affectées. Chaque fois qu’un contexte de certificat est dupliqué, son décompte de références est incrémenté d’une unité. Chaque fois qu’un pointeur vers un contexte de certificat est libéré, le nombre de références dans le contexte de certificat est décrémenté d’une unité. Lorsque le nombre de références sur un contexte de certificat atteint zéro, la mémoire contenant le contexte est désallouée. La mémoire allouée pour un contexte de certificat est également désallouée lorsque ce contexte se trouve dans un magasin et que le magasin est fermé à l’aide de l’indicateur de force du magasin de fermeture de certificat \_ \_ \_ \_ . Si la mémoire d’un contexte est désallouée et que les pointeurs vers ce contexte sont toujours en cours d’utilisation, ces pointeurs ne sont plus valides.

 

[**CertDuplicateStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatestore) augmente le [*nombre de références*](../secgloss/r-gly.md) sur le magasin.

[**CertSaveStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsavestore) enregistre le contenu d’un magasin dans un fichier disque ou dans un emplacement de mémoire, et

[**CertControlStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore) gère un magasin pendant qu’il est ouvert. Une application avec un magasin ouvert peut être avertie lorsque l’état persistant de cette banque a été modifié par un autre processus. Cela peut se produire si de nouveaux certificats ont été copiés dans le magasin de l’ordinateur local à partir d’un ordinateur de contrôle de domaine.

Lorsque des modifications sont découvertes, le magasin mis en cache peut resynchroniser son magasin mis en cache pour qu’il corresponde à l’état persistant du magasin. [**CertControlStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore) prend également en charge un processus qui copie les modifications apportées aux magasins mis en cache dans un stockage permanent lorsque ces modifications dans le magasin mis en cache ne sont pas enregistrées automatiquement.

Les contextes de certificat de type magasin de certificats peuvent avoir des propriétés étendues. [**CertSetStoreProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetstoreproperty) ajoute des propriétés étendues à un magasin de certificats. [**CertGetStoreProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetstoreproperty) récupère toutes les propriétés définies sur un magasin de certificats. Actuellement, la seule propriété de magasin de certificats prédéfinie est le nom localisé d’un magasin.

 

 
