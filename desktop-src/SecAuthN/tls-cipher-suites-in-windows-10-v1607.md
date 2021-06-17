---
description: En savoir plus sur les suites de chiffrement TLS dans Windows 10 v1607. Les suites de chiffrement ne peuvent être négociées que pour les versions TLS qui les prennent en charge.
ms.assetid: C7B6D1DE-E8CC-47EA-827A-A220F7AFB06B
title: Suites de chiffrement TLS dans Windows 10 v1607
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfc724d69bedb1b9092260f0c5e37b051c802b5f
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262491"
---
# <a name="tls-cipher-suites-in-windows-10-v1607"></a>Suites de chiffrement TLS dans Windows 10 v1607

Les suites de chiffrement ne peuvent être négociées que pour les versions TLS qui les prennent en charge. La version TLS la plus élevée prise en charge est toujours préférée dans la négociation TLS.

La disponibilité des suites de chiffrement doit être contrôlée de deux manières :

-   L’ordre de priorité par défaut est remplacé lors de la configuration d’une liste de priorités. Les suites de chiffrement qui ne sont pas dans la liste de priorités ne seront pas utilisées.
-   Autorisé lorsque l’application transmet SCH \_ utiliser \_ un \_ chiffrement fort : le fournisseur Microsoft Schannel filtre les suites de chiffrement faibles connues quand l’application utilise l' \_ \_ indicateur de chiffrement renforcé d’SCH use \_ . Dans Windows 10, version 1607 et Windows Server 2016, en plus des suites RC4, DES, exportation et chiffrement NULL sont filtrées.

> [!IMPORTANT]
> Les services Web HTTP/2 échouent avec les suites de chiffrement compatibles non-HTTP/2. Pour garantir la fonction de vos services Web avec les clients et les navigateurs HTTP/2, consultez Guide pratique [pour déployer le classement personnalisé des suites de chiffrement](https://support.microsoft.com/help/4032720/how-to-deploy-custom-cipher-suite-ordering-in-windows-server-2016).

 

La conformité FIPS est devenue plus complexe avec l’ajout de courbes elliptiques, ce qui rend la colonne activée en mode FIPS dans les versions précédentes de ce tableau trompeur. Par exemple, une suite de chiffrement telle que TLS \_ ECDHE \_ RSA \_ avec \_ AES \_ 128 \_ CBC \_ SHA256 est uniquement conforme aux normes FIPS lors de l’utilisation de courbes elliptiques NIST. Pour connaître les combinaisons de courbes elliptiques et de suites de chiffrement qui seront activées en mode FIPS, consultez la section 3.3.1 des [instructions relatives à la sélection, à la configuration et à l’utilisation des implémentations TLS]( https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-52r1.pdf).

Pour Windows 10, version 1607 et Windows Server 2016, les suites de chiffrement suivantes sont activées et dans cet ordre de priorité par défaut, utilisez le fournisseur Microsoft Schannel :



| Chaîne de la suite de chiffrement                                                                                 | Autorisé par SCH \_ utiliser \_ un \_ chiffrement renforcé | Versions du protocole TLS/SSL                     |
|-----------------------------------------------------------------------------------------------------|-------------------------------------|-----------------------------------------------|
| TLS \_ ECDHE \_ ECDSA \_ avec \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                           | Oui<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ avec \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                           | Oui<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ avec \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                             | Oui<br/>                      | TLS 1.2<br/>                            |
| \_ECDHE TLS \_ RSA \_ avec \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                             | Oui<br/>                      | TLS 1.2<br/>                            |
| TLS \_ dhe \_ RSA \_ avec \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                               | Oui<br/>                      | TLS 1.2<br/>                            |
| \_Dhe TLS \_ RSA \_ avec \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                               | Oui<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ avec \_ AES \_ 256 \_ CBC \_ SHA384<br/>                                           | Oui<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ avec \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                           | Oui<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ avec \_ AES \_ 256 \_ CBC \_ SHA384<br/>                                             | Oui<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ avec \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                             | Oui<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ avec \_ AES \_ 256 \_ CBC \_ SHA<br/>                                              | Oui<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ avec \_ AES \_ 128 \_ CBC \_ SHA<br/>                                              | Oui<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ avec \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                | Oui<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ avec \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                | Oui<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ dhe \_ RSA \_ avec \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                  | Oui<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ dhe \_ RSA \_ avec \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                  | Oui<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ RSA \_ avec \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                                    | Oui<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ avec \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                                    | Oui<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ avec \_ AES \_ 256 \_ CBC \_ SHA256<br/>                                                    | Oui<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ avec \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                                    | Oui<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ avec \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                       | Oui<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ RSA \_ avec \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                       | Oui<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ RSA \_ avec \_ 3DES \_ Ede \_ CBC \_ SHA<br/>                                                      | Oui<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ dhe \_ DSS \_ avec \_ AES \_ 256 \_ CBC \_ SHA256<br/>                                               | Oui<br/>                      | TLS 1.2<br/>                            |
| TLS \_ dhe \_ DSS \_ avec \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                               | Oui<br/>                      | TLS 1.2<br/>                            |
| TLS \_ dhe \_ DSS \_ avec \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                  | Oui<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ dhe \_ DSS \_ avec \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                  | Oui<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ dhe \_ DSS \_ avec \_ 3DES \_ Ede \_ CBC \_ SHA<br/>                                                 | Oui<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ avec \_ RC4 \_ 128 \_ SHA<br/>                                                            | Non<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ avec \_ RC4 \_ 128 \_ MD5<br/>                                                            | Non<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ avec \_ null \_ SHA256 <br/> Utilisé uniquement lorsque l’application demande explicitement.<br/> | Non<br/>                       | TLS 1.2<br/>                            |
| TLS \_ RSA \_ avec \_ \_ SHA null <br/> Utilisé uniquement lorsque l’application demande explicitement.<br/>    | Non<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |



 

Les suites de chiffrement suivantes sont prises en charge par le fournisseur Microsoft Schannel, mais ne sont pas activées par défaut :



| Chaîne de la suite de chiffrement                                                                              | Autorisé par SCH \_ utiliser \_ un \_ chiffrement renforcé | Versions du protocole TLS/SSL                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------|-----------------------------------------------|
| TLS \_ RSA \_ avec \_ des \_ CBC \_ SHA<br/>                                                         | Non<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ EXPORT1024 \_ avec \_ RC4 \_ 56 \_ SHA<br/>                                              | Non<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ EXPORT1024 \_ avec \_ des \_ CBC \_ SHA<br/>                                             | Non<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| \_Exportation RSA \_ TLS \_ avec \_ RC4 \_ 40 \_ MD5<br/>                                                  | Non<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ avec \_ \_ MD5 null <br/> Utilisé uniquement lorsque l’application demande explicitement.<br/> | Non<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ dhe \_ DSS \_ avec \_ des \_ CBC \_ SHA<br/>                                                    | Non<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ dhe \_ DSS \_ EXPORT1024 \_ avec \_ des \_ CBC \_ SHA<br/>                                        | Non<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |



 

À compter de Windows 10, version 1607 et Windows Server 2016, les suites de chiffrement PSK suivantes sont activées et, par défaut, dans cet ordre de priorité, utilisez le fournisseur Microsoft Schannel :



| Chaîne de la suite de chiffrement                              | Autorisé par SCH \_ utiliser \_ un \_ chiffrement renforcé | Versions du protocole TLS/SSL |
|--------------------------------------------------|-------------------------------------|---------------------------|
| TLS \_ PSK \_ avec \_ AES \_ 256 \_ GCM \_ SHA384<br/> | Oui<br/>                      | TLS 1.2<br/>        |
| TLS \_ PSK \_ avec \_ AES \_ 128 \_ GCM \_ SHA256<br/> | Oui<br/>                      | TLS 1.2<br/>        |
| TLS \_ PSK \_ avec \_ AES \_ 256 \_ CBC \_ SHA384<br/> | Oui<br/>                      | TLS 1.2<br/>        |
| TLS \_ PSK \_ avec \_ AES \_ 128 \_ CBC \_ SHA256<br/> | Oui<br/>                      | TLS 1.2<br/>        |
| TLS \_ PSK \_ avec \_ null \_ SHA384<br/>          | Non<br/>                       | TLS 1.2<br/>        |
| TLS \_ PSK \_ avec \_ null \_ SHA256<br/>          | Non<br/>                       | TLS 1.2<br/>        |



 

> [!Note]  
> Aucune suite de chiffrement PSK n’est activée par défaut. Les applications doivent demander PSK avec l' \_ utilisation de \_ PRESHAREDKEY \_ uniquement. Pour plus d’informations sur les indicateurs Schannel, consultez [**Schannel \_ cred**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred).

 

Pour ajouter des suites de chiffrement, déployez une stratégie de groupe ou utilisez les applets de commande TLS :

-   Pour utiliser la stratégie de groupe, configurez l’ordre de la suite de chiffrement SSL sous Configuration ordinateur > Modèles d’administration > paramètres de configuration du réseau > SSL avec la liste priorité pour toutes les suites de chiffrement que vous souhaitez activer.
-   Pour utiliser PowerShell, consultez [applets](/powershell/module/tls/?view=win10-ps)de commande TLS.

> [!Note]  
> Avant Windows 10, les chaînes de suite de chiffrement étaient ajoutées à la courbe elliptique pour déterminer la priorité de la courbe. Windows 10 prend en charge un paramètre d’ordre de priorité de courbe elliptique, ce qui signifie que le suffixe de courbe elliptique n’est pas obligatoire et est remplacé par le nouvel ordre de priorité de la courbe elliptique, le cas échéant, pour permettre aux organisations d’utiliser la stratégie de groupe pour configurer différentes versions de Windows avec les mêmes suites de chiffrement.

 

 

 
