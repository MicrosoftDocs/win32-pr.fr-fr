---
description: Le magasin de certificats est central pour toutes les opérations de gestion des certificats.
ms.assetid: e5c7c882-cbfc-4343-952c-b13c67326756
title: Extension de la fonctionnalité CertOpenStore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c770ae56ff597f51248486db2c9eb2d74bea8d63d2e8daad83d5938594b2f1a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007084"
---
# <a name="extending-certopenstore-functionality"></a>Extension de la fonctionnalité CertOpenStore

Le [*magasin de certificats*](../secgloss/c-gly.md) est central pour toutes les opérations de gestion des certificats. Les fonctionnalités de la fonction [**CertOpenStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certopenstore) peuvent être étendues à l’aide d’une fonction de fournisseur de magasin de certificats installable (ou inscrite). Pour obtenir une vue d’ensemble de l’installation ou de l’inscription des fonctions à utiliser avec CryptoAPI, consultez [vue d’ensemble des OID](oid-overview.md).

> [!Note]  
> Les magasins de certificats personnalisés ne sont pas automatiquement migrés lors de l’exécution de déploiements automatisés. pour migrer des magasins de certificats personnalisés, vous devez créer un manifeste pour la migration des magasins personnalisés et utiliser le Outil de migration utilisateur Windows (USMT). L’outil USMT peut être téléchargé à partir du centre de téléchargement Microsoft à l’adresse <https://www.microsoft.com/download/details.aspx?id=10837> .

 

[**CertOpenStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certopenstore) ouvre un magasin vide en mémoire et appelle la fonction du fournisseur de magasin (s’il est inscrit ou installé) à l’aide de l' [*identificateur d’objet*](../secgloss/o-gly.md) (OID) qui a été transmis dans le paramètre *lpszStoreProvider* . Pour obtenir la liste des types de fournisseurs prédéfinis fournis avec l’CryptoAPI, consultez **CertOpenStore**.

La fonction du fournisseur de magasin copie ses certificats et [*listes de révocation de certificats*](../secgloss/c-gly.md) (CRL) vers le magasin en mémoire spécifié par le handle *hCertStore* qui lui est passé. La nouvelle fonction de fournisseur de magasin peut utiliser toutes les fonctions du magasin de certificats CryptoAPI, telles que [**CertAddCertificateContextToStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certaddcertificatecontexttostore) ou [**CertAddSerializedElementToStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certaddserializedelementtostore), pour ajouter ses certificats et listes de révocation de certificats au magasin en mémoire. En outre, la fonction du fournisseur de magasin retourne éventuellement des valeurs pour tous les membres de données de la structure d' [**\_ \_ \_ informations Prov du magasin de certificats**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_store_prov_info) . La fonction doit uniquement mettre à jour cette structure si elle prend en charge des fonctions de rappel supplémentaires. Par exemple, si le magasin doit être un magasin en lecture seule, la prise en charge d’autres fonctions de rappel n’est probablement pas nécessaire. Pour plus d’informations et pour les prototypes des fonctions de rappel possibles, consultez [fonctions de rappel du fournisseur du magasin de certificats](cryptography-functions.md).

Le magasin TrustedPeople par utilisateur est limité aux magasins physiques prédéfinis. Vous ne pouvez pas étendre le magasin TrustedPeople par utilisateur. Toutefois, vous pouvez étendre le magasin TrustedPeople de l’ordinateur local.

**Windows XP et Windows Server 2003 :** Le magasin TrustedPeople par utilisateur n’est pas limité aux magasins physiques prédéfinis.

L’un des membres de données de la structure [**\_ \_ Prov \_ info du magasin de certificats**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_store_prov_info) est le tableau *rgpvStoreProvFunc* . Si la fonction du fournisseur de magasin doit prendre en charge une ou plusieurs des fonctions de rappel, elle doit fournir des pointeurs pour ce tableau. Ces pointeurs doivent pointer vers les fonctions de rappel qui doivent être utilisées pour d’autres activités de magasin de certificats (telles que la fermeture du magasin). L’illustration suivante montre le déroulement de ce processus.

![fonctionnalité CertOpenStore](images/openstor.png)

Comme indiqué dans l’illustration suivante, une fois le magasin ouvert, les autres fonctions CryptoAPI (telles que [**CertCloseStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certclosestore)) utilisent le tableau de pointeurs pour accéder aux fonctions de rappel qui exécutent la tâche prévue. La définition de la [**structure \_ \_ Prov \_ info du magasin**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_store_prov_info) de certificats et les prototypes des fonctions de rappel par défaut qui sont fournies avec l’CryptoAPI sont affichées dans les fonctions de rappel du fournisseur du magasin de [certificats](cryptography-functions.md).

![fonctionnalité certclosestore](images/closstor.png)

Les API de stockage permettent à un fournisseur de magasins de conserver les certificats, les listes de révocation de certificats et les listes de certificats de [*confiance*](../secgloss/c-gly.md) (CTL) à l’extérieur du cache du magasin (par exemple, une base de données externe de certificats, telle que fournie par la base de données du serveur de certificats Microsoft).

[**CertOpenStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certopenstore) distribue via le paramètre *pszStoreProvider* à la fonction de fournisseur d’installation [**CertDllOpenStoreProv**](/windows/win32/api/Wincrypt/nc-wincrypt-pfn_cert_dll_open_store_prov_func) appropriée. Le fournisseur retourne des informations dans le paramètre *pStoreProvInfo* qui pointe vers une structure [**\_ \_ Prov \_ info de magasin de certificats**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_store_prov_info) . La structure de l' **\_ \_ \_ information Prov Store store** contient un membre **dwStoreProvFlags** . L’indicateur de l' \_ indicateur externe Prov. du magasin de certificats \_ \_ \_ a été ajouté pour permettre au fournisseur d’indiquer que les certificats, les listes de révocation de certificats et les listes de certificats de confiance sont externes au cache du magasin.

[**CertDllOpenStoreProv**](/windows/win32/api/Wincrypt/nc-wincrypt-pfn_cert_dll_open_store_prov_func) retourne un tableau de fonctions de rappel. Un fournisseur peut implémenter les fonctions de rappel suivantes :

-   fin de la fonction de clôture du magasin de certificats \_ \_ \_ \_
-   certificat du magasin de certificats \_ \_ Proven \_ lire le \_ certificat \_
-   certificat du magasin de certificats \_ \_ Proven \_ Write \_ \_
-   certificat du magasin de certificats \_ \_ Prov \_ supprimer le \_ certificat \_
-   propriété de certificat du magasin de certificats \_ \_ Prov \_ Set \_ \_ \_
-   \_ \_ \_ lecture \_ de la liste de révocation de certificats \_ du magasin de certificats
-   \_Func d' \_ \_ écriture de la \_ liste de révocation de certificats \_ CERT Store
-   fonction \_ \_ \_ \_ de suppression de la liste de révocation de certificats \_ CERT Store Prov
-   \_ \_ \_ valeur \_ de la propriété de la liste de révocation de certificats \_ \_ du magasin de certificats
-   \_mode de \_ \_ lecture \_ CTL \_ PROVen du magasin de certificats
-   fonction \_ \_ CTL d' \_ écriture \_ CTL \_ du magasin de certificats
-   Banque de certificats \_ \_ Prov- \_ Delete \_ CTL \_ Func
-   propriété de la liste de certificats de confiance du magasin de certificats \_ \_ \_ \_ \_ \_

Sur les appels au certificat d’écriture, à la \_ \_ liste de révocation des certificats d’écriture et aux fonctions de rappel d’écriture \_ CTL lorsque l' \_ indicateur d' \_ écriture Proven Write du magasin \_ de certificats \_ \_ est défini, les 16 bits supérieurs du paramètre *dwFlags* contiennent la valeur *dwAddDisposition* . Pour prendre en charge les magasins externes, un fournisseur peut implémenter les fonctions de rappel suivantes :

-   CERT \_ Store \_ Prov \_ Rechercher \_ CERT \_ Func
-   CERT \_ Store \_ Prov \_ gratuit \_ trouver le \_ certificat \_
-   propriété d’extraction de certificat de la Banque de certificats \_ \_ Prov \_ \_ \_ \_
-   fonction \_ \_ de la \_ \_ liste de révocation de certificats \_ du magasin de certificats Prov
-   la \_ \_ \_ \_ \_ liste de révocation de certificats du magasin de certificats Prov gratuit Find \_
-   \_ \_ \_ \_ propriété de la liste de révocation des certificats du magasin de certificats \_ Prov \_
-   \_Banque CERT \_ Store \_ Prov \_ \_
-   \_liste CTL de la \_ \_ \_ recherche \_ gratuite \_ de la boutique du magasin de certificats
-   propriété d’extraction de la liste de certificats de confiance du magasin de certificats \_ \_ \_ \_ \_ \_

Les fonctions de rappel de certificat ont les signatures suivantes :

``` syntax
typedef struct _CERT_STORE_PROV_FIND_INFO {
    DWORD               cbSize;
    DWORD               dwMsgAndCertEncodingType;
    DWORD               dwFindFlags;
    DWORD               dwFindType;
    const void          *pvFindPara;
} CERT_STORE_PROV_FIND_INFO, *PCERT_STORE_PROV_FIND_INFO;
typedef const CERT_STORE_PROV_FIND_INFO CCERT_STORE_PROV_FIND_INFO,
    *PCCERT_STORE_PROV_FIND_INFO;

typedef BOOL (WINAPI *PFN_CERT_STORE_PROV_FIND_CERT)(
        IN HCERTSTOREPROV hStoreProv,
        IN PCCERT_STORE_PROV_FIND_INFO pFindInfo,
        IN PCCERT_CONTEXT pPrevCertContext,
        IN DWORD dwFlags,
        IN OUT void **ppvStoreProvFindInfo,
        OUT PCCERT_CONTEXT *ppProvCertContext
        );

typedef BOOL (WINAPI *PFN_CERT_STORE_PROV_FREE_FIND_CERT)(
        IN HCERTSTOREPROV hStoreProv,
        IN PCCERT_CONTEXT pCertContext,
        IN void *pvStoreProvFindInfo,
        IN DWORD dwFlags
        );

typedef BOOL (WINAPI *PFN_CERT_STORE_PROV_GET_CERT_PROPERTY)(
        IN HCERTSTOREPROV hStoreProv,
        IN PCCERT_CONTEXT pCertContext,
        IN DWORD dwPropId,
        IN DWORD dwFlags,
        OUT void *pvData,
        IN OUT DWORD *pcbData
        );
```

Les signatures de la liste de révocation de certificats et des fonctions de rappel CTL sont identiques à celles ci-dessus avec le pointeur vers le [**\_ contexte de certificat**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) remplacé par un pointeur vers un contexte [**de liste de révocation de certificats \_**](/windows/win32/api/Wincrypt/ns-wincrypt-crl_context) ou un [**\_ contexte**](/windows/win32/api/Wincrypt/ns-wincrypt-ctl_context)de liste CTL.

Le rappel de la recherche de \_ certificat est appelé quand les API du Store énumèrent, recherchent ou ajoutent des certificats. *pPrevCertContext* et *ppvStoreProvFindInfo* ont la valeur **null** pour lancer une nouvelle recherche. Le *ppvStoreProvFindInfo* retourné est retransmis à la prochaine recherche, à laquelle il peut être libéré par le fournisseur. Le fournisseur peut définir tout, une partie ou aucune des propriétés du certificat. Le fournisseur a la possibilité de différer jusqu’à ce que le rappel de propriété obtention du \_ certificat \_ soit appelé. Il est recommandé aux fournisseurs de définir autant de propriétés que possible pour permettre la copie dans un autre magasin.

Les types de recherche de certificat suivants sont pris en charge dans [**CertFindCertificateInStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certfindcertificateinstore):

-   CERTIFICAT \_ trouvé \_ tout
-   CERT- \_ Rechercher le \_ \_ hachage SHA1
-   \_ \_ Hachage MD5 de la recherche de certificat \_
-   \_propriété de recherche de certificat \_
-   \_ \_ clé publique de recherche de certificat \_
-   nom de l’objet de recherche de certificat \_ \_ \_
-   ATTR de l’objet de recherche de certificat \_ \_ \_
-   nom de l’émetteur de recherche de certificat \_ \_ \_
-   CERT \_ Rechercher l' \_ émetteur \_ attr
-   CERT \_ Rechercher l' \_ objet \_ Str \_ A
-   chaîne d’objet de recherche de CERT \_ \_ \_ \_ W
-   CERT \_ Rechercher l' \_ émetteur \_ Str \_ A
-   CERT- \_ Rechercher l' \_ émetteur \_ Str \_ W
-   spécification de la clé de recherche de certificat \_ \_ \_
-   \_ \_ utilisation ENHKEY de la recherche de certificat \_

Le rappel de la recherche de \_ certificat est appelé pour chacun des types de recherche ci-dessus. Les paramètres passés à [**CertFindCertificateInStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certfindcertificateinstore) sont copiés directement dans la \_ structure de la prove du magasin de certificats \_ \_ \_ avant l’appel de la recherche de \_ rappel de certificat. Pour plus d’informations sur les valeurs de champ pour les différents types de recherche de la \_ \_ structure PROV (informations de recherche) du magasin de certificats \_ \_ , consultez **CertFindCertificateInStore**.

Les types de recherche de certificat suivants prennent en charge les API [**CertGetSubjectCertificateFromStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certgetsubjectcertificatefromstore) et [**CertGetIssuerCertificateFromStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certgetissuercertificatefromstore) et aident à déterminer si le certificat existe déjà dans le magasin avant d’ajouter :

-   CERT- \_ Rechercher le \_ sujet du \_ certificat
-   CERT \_ Find \_ émetteur \_ de
-   Rechercher le certificat \_ \_ existant

Pour le \_ certificat de l’objet CERT Find \_ \_ , le paramètre *pvFindPara* pointe vers une structure d' [**\_ informations de certificat**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_info) qui contient l’émetteur et le numéro de série de l’objet. Pour \_ l’émetteur de la recherche de certificat, \_ \_ *pvFindPara* pointe vers une structure de [**\_ contexte de certificat**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) , de l’objet. Pour CERT \_ Find \_ existing, *pvFindPara* pointe vers **un \_ contexte** de certificat du certificat afin de vérifier son existence dans le magasin.

Le rappel de certificat gratuit de \_ recherche \_ est appelé lorsque le certificat retourné par le rappel de la recherche de certificat \_ n’a pas été libéré en étant utilisé dans un autre certificat de recherche suivant \_ , dont le [*nombre de références*](../secgloss/r-gly.md) est décrémenté à zéro, ou en étant libéré par un appel à [**CertCloseStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certclosestore). Avant que le rappel de fermeture ne soit appelé, tous les certificats retournés par le \_ rappel de recherche de certificat doivent être libérés pour le fournisseur en passant à un appel au rappel de recherche de \_ certificat ou à un appel au \_ rappel de certificat de recherche libre \_ . Il en va de même pour la liste de révocation de certificats et les rappels CTL.

Le \_ rappel de \_ propriété obtenir le certificat est appelé par [**CertGetCertificateContextProperty**](/windows/win32/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) s’il ne peut pas trouver la propriété spécifiée pour le paramètre *pCertContext* . Il en va de même pour les propriétés obtenir la \_ liste de révocation de certificats \_ et obtenir la liste \_ CTL \_ .

Le rappel Rechercher une \_ liste de révocation de certificats est appelé quand les API du Store énumèrent ou obtiennent des listes de révocation de certificats et avant d’ajouter une liste Les types de recherche de la liste de révocation de certificats suivants sont définis :

Pour la recherche de liste de révocation de certificats \_ \_ émise \_ par, *pvFindPara* est un pointeur vers un [**\_ contexte de certificat**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) de l’émetteur de la liste de révocation de certificats. Pour la liste de révocation de certificats \_ \_ existante, *pvFindPara* est un pointeur vers un [**\_ contexte de liste**](/windows/win32/api/Wincrypt/ns-wincrypt-crl_context) de révocation de certificats de la liste de révocation de certificats pour déterminer si elle existe déjà dans le magasin.

Le rappel de la \_ liste de certificats de confiance est appelé quand les API du magasin énumèrent ou recherchent des listes CTL. Les types de listes de certificats de confiance suivants sont pris en charge dans [**CertFindCTLInStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certfindctlinstore):

-   liste CTL \_ Rechercher \_
-   CTL \_ Rechercher \_ le \_ hachage SHA1
-   CTL \_ Rechercher \_ le \_ hachage MD5
-   liste CTL \_ Rechercher \_ l’utilisation
-   liste CTL \_ Rechercher l' \_ objet
-   liste CTL \_ Rechercher l' \_ existante

Le rappel de la liste de certificats de recherche \_ est appelé pour chacun des types de recherche ci-dessus. Les paramètres passés à [**CertFindCTLInStore**](/windows/win32/api/Wincrypt/nf-wincrypt-certfindctlinstore) sont copiés directement dans la structure de la prove de la boutique du magasin de certificats \_ \_ \_ \_ avant l’appel du rappel de la \_ liste de certificats de confiance. Pour plus d’informations sur les valeurs de champ pour les différents types de recherche de la \_ \_ structure PROV (informations de recherche) du magasin de certificats \_ \_ , consultez **CertFindCTLInStore**.

Le type de liste CTL \_ Rechercher un \_ type de liste CTL existant permet de déterminer si la liste CTL existe déjà dans le magasin avant d’ajouter une liste de certificats de confiance.

Pour la liste de certificats de confiance \_ \_ existante, *pvFindPara* est un pointeur vers la structure de [**\_ contexte CTL**](/windows/win32/api/Wincrypt/ns-wincrypt-ctl_context) de la liste CTL pour déterminer si elle existe déjà dans le magasin.

 

 
