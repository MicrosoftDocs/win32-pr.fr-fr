---
description: Un magasin système est un regroupement qui se compose d’un ou de plusieurs magasins frères physiques.
ms.assetid: 41fe9366-4c17-43bb-91d6-934c7aa87a2d
title: Emplacements du magasin système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0863ffde8be5db67459908b1ec26ec73da029744
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095838"
---
# <a name="system-store-locations"></a>Emplacements du magasin système

Un magasin système est un regroupement qui se compose d’un ou de plusieurs magasins frères physiques. Pour chaque magasin système, il existe des magasins frères physiques prédéfinis. Après l’ouverture d’un magasin système comme MY at CERT \_ System \_ Store \_ Current \_ User, le fournisseur Store appelle [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) pour ouvrir chacun des magasins physiques dans le regroupement du magasin système. Dans le processus ouvert, chacun de ces magasins physiques est ajouté au regroupement du magasin système à l’aide de [**CertAddStoreToCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddstoretocollection). Tous les certificats de ces magasins physiques sont disponibles par le biais du regroupement du magasin de système logique.

Pour chaque emplacement du magasin système, les magasins de systèmes prédéfinis sont les suivants :

-   MY
-   Root
-   Confiance
-   CA

Dans l' \_ \_ utilisateur actuel du magasin système CERT \_ \_ , il existe également un magasin UserDS prédéfini. Un magasin de cartes à puce est prévu pour cet emplacement.

Voici les magasins système suivis par d’autres remarques :

-   [\_magasin système du certificat \_ \_ \_ utilisateur actuel](#cert_system_store_current_user)
-   [\_ \_ ordinateur local du magasin système \_ du \_ certificat](#cert_system_store_local_machine)
-   [\_service du magasin système du certificat \_ \_ actuel \_](#cert_system_store_current_service)
-   [\_services du \_ magasin \_ système du certificat](#cert_system_store_services)
-   [\_utilisateurs du \_ magasin \_ système du certificat](#cert_system_store_users)
-   [stratégie de groupe de l' \_ \_ utilisateur actuel du système CERT \_ \_ \_](#cert_system_current_user_group_policy)
-   [stratégie de groupe de l' \_ \_ ordinateur local du système CERT \_ \_ \_](#cert_system_local_machine_group_policy)
-   [CERT \_ System \_ Store \_ local \_ machine \_ Enterprise](#cert_system_store_local_machine_enterprise)
-   [Remarques](#remarks)

### <a name="cert_system_store_current_user"></a>\_magasin système du certificat \_ \_ \_ utilisateur actuel

\_Magasin système de certificats \_ \_ \_ les magasins système de l’utilisateur actuel se trouvent à l’emplacement de Registre suivant :

```
HKEY_CURRENT_USER
   Software
      Microsoft
         SystemCertificates
```

Les magasins physiques prédéfinis associés à ces magasins système sont les suivants :



| Magasin système | Magasin physique                                           |
|--------------|----------------------------------------------------------|
| MY           | . Valeurs                                                 |
| Root         | . Default. LocalMachine<br/> . Carte à puce<br/>   |
| Confiance        | . Default. GroupPolicy<br/> . LocalMachine<br/> |
| CA           | . Default. GroupPolicy<br/> . LocalMachine<br/> |
| UserDS       | . UserCertificate                                         |



 

### <a name="cert_system_store_local_machine"></a>\_ \_ ordinateur local du magasin système \_ du \_ certificat

\_ \_ \_ \_ Les magasins du système de l’ordinateur local du magasin système du certificat se trouvent à l’emplacement de Registre suivant :

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         SystemCertificates
```

Les magasins physiques prédéfinis sont associés à ces magasins système, comme indiqué ci-dessous.



| Magasin système | Magasin physique                                                                                    |
|--------------|---------------------------------------------------------------------------------------------------|
| MY           | . Valeurs                                                                                          |
| Root         | . Default. AuthRoot<br/> . GroupPolicy<br/> . Enterprise<br/> . Carte à puce<br/> |
| Confiance        | . Default. GroupPolicy<br/> . Enterprise<br/>                                            |
| CA           | . Default. GroupPolicy<br/> . Enterprise <br/>                                           |



 

### <a name="cert_system_store_current_service"></a>\_service du magasin système du certificat \_ \_ actuel \_

\_ \_ \_ \_ Les magasins du système de service du magasin système du certificat actuel se trouvent à l’emplacement de Registre suivant :

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Cryptography
            Services
               ServiceName
                  SystemCertificates
```

Les magasins physiques prédéfinis associés à ces magasins système sont les suivants :



| Magasin système | Magasin physique                   |
|--------------|----------------------------------|
| MY           | . Valeurs                         |
| Root         | . Default. LocalMachine<br/> |
| Confiance        | . Default. LocalMachine<br/> |
| CA           | . Default. LocalMachine<br/> |



 

### <a name="cert_system_store_services"></a>\_services du \_ magasin \_ système du certificat

\_ \_ \_ Les magasins système des services du magasin système de certificats se trouvent à l’emplacement de Registre suivant :

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Cryptography
            Services
               ServiceName
                  SystemCertificates
```

Les magasins physiques prédéfinis associés à ces magasins système sont les suivants :



| Magasin système       | Magasin physique                   |
|--------------------|----------------------------------|
| ServiceName \\ My    | . Valeurs                         |
| \\Racine ServiceName  | . Default. LocalMachine<br/> |
| \\Confiance ServiceName | . Default. LocalMachine<br/> |
| \\AC ServiceName    | . Default. LocalMachine<br/> |



 

### <a name="cert_system_store_users"></a>\_utilisateurs du \_ magasin \_ système du certificat

\_ \_ \_ Les magasins système des utilisateurs du magasin système du certificat se trouvent à l’emplacement de Registre suivant :

```
HKEY_USERS
   UserName
      Software
         Microsoft
            SystemCertificates
```

Les magasins physiques prédéfinis associés à ces magasins système sont les suivants :



| Magasin système  | Magasin physique                   |
|---------------|----------------------------------|
| userid \\ My    | . Default. LocalMachine<br/> |
| \\racine userid  | . Default. LocalMachine<br/> |
| \\confiance userid | . Default. LocalMachine<br/> |
| ID de l' \\ autorité de certification    | . Default. LocalMachine<br/> |



 

### <a name="cert_system_current_user_group_policy"></a>stratégie de groupe de l' \_ \_ utilisateur actuel du système CERT \_ \_ \_

\_Système de \_ certificats \_ \_ \_ les banques système de la stratégie de groupe de l’utilisateur actuel se trouvent à l’emplacement de Registre suivant :

```
HKEY_CURRENT_USER
   Software
      Policy
         Microsoft
            SystemCertificates
```

### <a name="cert_system_local_machine_group_policy"></a>stratégie de groupe de l' \_ \_ ordinateur local du système CERT \_ \_ \_

\_ \_ \_ \_ \_ Les banques système de la stratégie de groupe de l’ordinateur local du certificat se trouvent à l’emplacement de Registre suivant :

```
HKEY_LOCAL_MACHINE
   Software
      Policy
         Microsoft
            SystemCertificates
```

### <a name="cert_system_store_local_machine_enterprise"></a>CERT \_ System \_ Store \_ local \_ machine \_ Enterprise

CERT \_ System \_ Store \_ local \_ machine \_ Enterprise contient les certificats partagés entre les domaines de l’entreprise et téléchargés à partir de l’annuaire global de l’entreprise. Pour synchroniser le magasin de l’entreprise du client, l’annuaire d’entreprise est interrogé toutes les huit heures et les certificats sont téléchargés automatiquement en arrière-plan.

Les magasins physiques prédéfinis associés à ces magasins système sont les suivants :



| Magasin système | Magasin physique |
|--------------|----------------|
| MY           | . Valeurs       |
| Root         | . Valeurs       |
| Confiance        | . Valeurs       |
| CA           | . Valeurs       |



 

### <a name="remarks"></a>Notes

Des magasins physiques supplémentaires peuvent être associés à un magasin système à l’aide de [**CertRegisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregisterphysicalstore).

Les \_ magasins de certificats du magasin système \_ \_ et \_ \_ \_ d’utilisateurs du magasin système du certificat sont ouverts en préfixant le nom du magasin dans la chaîne transmise à *pvPara* avec le nom de service ou d’utilisateur, tel que *ServiceName* \\ **Trust** ou **. Par défaut** \\ **My**. L’emplacement des utilisateurs du magasin du système \_ \_ de certificats \_ ou des services du magasin système de certificats \_ \_ \_ peut ouvrir le même magasin dans le service actuel du système de certificats ou dans le \_ \_ \_ \_ \_ magasin système de certificats de l' \_ utilisateur actuel à \_ l’aide de l' [*identificateur de sécurité*](../secgloss/s-gly.md) textuel (SID) du service ou de l’utilisateur actuel.

Les magasins dans la stratégie de \_ groupe d’utilisateurs du magasin système du certificat \_ \_ \_ \_ et \_ \_ \_ \_ \_ la stratégie de groupe de l’ordinateur local du système de certificats dans un paramètre réseau sont téléchargés sur l’ordinateur client à partir du modèle de stratégie de groupe (GPT) lors du démarrage de l’ordinateur ou de l’ouverture de session utilisateur. Ces magasins peuvent être mis à jour sur l’ordinateur client après le démarrage ou l’ouverture de session lorsque le GPT est modifié sur le serveur de domaine par un administrateur. La fonction [**CertControlStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore) permet à une application d’être avertie lorsque des magasins dans l’un de ces emplacements ont changé.

Les emplacements du magasin système suivants peuvent être ouverts à distance :

-   \_ \_ ordinateur local du magasin système \_ du \_ certificat
-   stratégie de groupe de l' \_ \_ \_ ordinateur local du magasin système \_ \_ du \_ certificat
-   \_services du \_ magasin \_ système du certificat
-   \_utilisateurs du \_ magasin \_ système du certificat

Les emplacements du magasin système sont ouverts à distance en préfixant le nom du magasin dans la chaîne transmise à *pvPara* par le nom de l’ordinateur. Voici des exemples de noms de magasins système distants :

-   *Nom de l’ordinateur* \\ **Autorité de certification**
-   \\\\*Nom de l’ordinateur* \\ **Autorité de certification**
-   *Nom de l’ordinateur* \\ *ServiceName* \\ Niveau de **confiance**
-   \\\\*Nom de l’ordinateur* \\ *ServiceName* \\ Niveau de **confiance**

 

 
