---
description: Les suites de chiffrement ne peuvent être négociées que pour les versions TLS qui les prennent en charge.
ms.assetid: F37C3596-E273-4144-87B9-D589EBB82C0B
title: Suites de chiffrement TLS dans Windows 8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8613c018857525f7877e883f21b1eea7bd53e55a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867449"
---
# <a name="tls-cipher-suites-in-windows-8"></a>Suites de chiffrement TLS dans Windows 8

Les suites de chiffrement ne peuvent être négociées que pour les versions TLS qui les prennent en charge. La version TLS la plus élevée prise en charge est toujours préférée dans la négociation TLS. Par exemple, SSL \_ CK \_ RC4 \_ 128 \_ avec \_ MD5 ne peut être utilisé que si le client et le serveur ne prennent pas en charge TLS 1,2, 1,1 & 1,0 ou SSL 3,0 puisqu’il est uniquement pris en charge avec SSL 2,0.

La disponibilité des suites de chiffrement doit être contrôlée de deux manières :

-   L’ordre de priorité par défaut est remplacé lors de la configuration d’une liste de priorités. Les suites de chiffrement qui ne sont pas dans la liste de priorités ne seront pas utilisées.
-   Autorisé lorsque l’application transmet \_ SCH \_ utiliser \_ un chiffrement fort : le fournisseur Microsoft Schannel filtre les suites de chiffrement faibles connues quand l’application utilise l' \_ \_ indicateur de chiffrement renforcé d’SCH use \_ . Dans Windows 8, les suites de chiffrement RC4 sont filtrées.

> [!IMPORTANT]
> Les services Web HTTP/2 échouent avec les suites de chiffrement compatibles non-HTTP/2. Pour garantir la fonction de vos services Web avec les clients et les navigateurs HTTP/2, consultez Guide pratique [pour déployer le classement personnalisé des suites de chiffrement](https://support.microsoft.com/help/4032720/how-to-deploy-custom-cipher-suite-ordering-in-windows-server-2016).

 

La conformité FIPS est devenue plus complexe avec l’ajout de courbes elliptiques, ce qui rend la colonne activée en mode FIPS dans les versions précédentes de ce tableau trompeur. Par exemple, une suite de chiffrement telle que TLS \_ ECDHE \_ RSA \_ avec \_ AES \_ 128 \_ CBC \_ SHA256 est uniquement conforme aux normes FIPS lors de l’utilisation de courbes elliptiques NIST. Pour connaître les combinaisons de courbes elliptiques et de suites de chiffrement qui seront activées en mode FIPS, consultez la section 3.3.1 des [instructions relatives à la sélection, à la configuration et à l’utilisation des implémentations TLS]( https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-52r1.pdf).

Windows 7, Windows 8 et Windows Server 2012 sont mis à jour par la Windows Update par la mise à jour 3042058, qui modifie l’ordre de priorité. Pour plus d’informations, consultez l' [avis de sécurité Microsoft 3042058](/security-updates/SecurityAdvisories/2015/3042058) . Les suites de chiffrement suivantes sont activées et, par défaut, dans cet ordre de priorité par le fournisseur Microsoft Schannel :



| Chaîne de la suite de chiffrement                                                                                            | Autorisé par SCH \_ utiliser \_ un \_ chiffrement renforcé | Versions du protocole TLS/SSL                     |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------|-----------------------------------------------|
| TLS \_ ECDHE \_ RSA \_ avec \_ AES \_ 256 \_ CBC \_ SHA384 \_ P256<br/>                                                  | Oui<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ avec \_ AES \_ 256 \_ CBC \_ SHA384 \_ P384<br/>                                                  | Oui<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ avec \_ AES \_ 128 \_ CBC \_ SHA256 \_ P256<br/>                                                  | Oui<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ avec \_ AES \_ 128 \_ CBC \_ SHA256 \_ P384<br/>                                                  | Oui<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ avec \_ AES \_ 256 \_ CBC \_ SHA \_ P256<br/>                                                     | Oui<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ avec \_ AES \_ 256 \_ CBC \_ SHA \_ P384<br/>                                                     | Oui<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ avec \_ AES \_ 128 \_ CBC \_ SHA \_ P256<br/>                                                     | Oui<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ avec \_ AES \_ 128 \_ CBC \_ SHA \_ P384<br/>                                                     | Oui<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ dhe \_ RSA \_ avec \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                                          | Oui<br/>                      | TLS 1.2<br/>                            |
| \_Dhe TLS \_ RSA \_ avec \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                                          | Oui<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ avec \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                                               | Oui<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ avec \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                                               | Oui<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ avec \_ AES \_ 256 \_ CBC \_ SHA256<br/>                                                               | Oui<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ avec \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                                               | Oui<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ avec \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                                  | Oui<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ RSA \_ avec \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                                  | Oui<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ avec \_ AES \_ 256 \_ GCM \_ SHA384 \_ P384<br/>                                                | Oui<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ avec \_ AES \_ 128 \_ GCM \_ SHA256 \_ P256<br/>                                                | Oui<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ avec \_ AES \_ 128 \_ GCM \_ SHA256 \_ P384<br/>                                                | Oui<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ avec \_ AES \_ 256 \_ CBC \_ SHA384 \_ P384<br/>                                                | Oui<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ avec \_ AES \_ 128 \_ CBC \_ SHA256 \_ P256<br/>                                                | Oui<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ avec \_ AES \_ 128 \_ CBC \_ SHA256 \_ P384<br/>                                                | Oui<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ avec \_ AES \_ 256 \_ CBC \_ SHA \_ P256<br/>                                                   | Oui<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ avec \_ AES \_ 256 \_ CBC \_ SHA \_ P384<br/>                                                   | Oui<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ avec \_ AES \_ 128 \_ CBC \_ SHA \_ P256<br/>                                                   | Oui<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ avec \_ AES \_ 128 \_ CBC \_ SHA \_ P384<br/>                                                   | Oui<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ dhe \_ DSS \_ avec \_ AES \_ 256 \_ CBC \_ SHA256<br/>                                                          | Oui<br/>                      | TLS 1.2<br/>                            |
| TLS \_ dhe \_ DSS \_ avec \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                                          | Oui<br/>                      | TLS 1.2<br/>                            |
| TLS \_ dhe \_ DSS \_ avec \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                             | Oui<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ dhe \_ DSS \_ avec \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                             | Oui<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ RSA \_ avec \_ 3DES \_ Ede \_ CBC \_ SHA<br/>                                                                 | Oui<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ dhe \_ DSS \_ avec \_ 3DES \_ Ede \_ CBC \_ SHA<br/>                                                            | Oui<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ avec \_ RC4 \_ 128 \_ SHA<br/>                                                                       | Non<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ avec \_ RC4 \_ 128 \_ MD5<br/>                                                                       | Non<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ avec \_ null \_ SHA256 <br/> Utilisé uniquement lorsque l’application demande explicitement.<br/>            | Oui<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ avec \_ \_ SHA null <br/> Utilisé uniquement lorsque l’application demande explicitement.<br/>               | Oui<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| SSL \_ CK \_ RC4 \_ 128 \_ avec \_ MD5 <br/> Utilisé uniquement lorsque l’application demande explicitement.<br/>            | Non<br/>                       | SSL 2.0<br/>                            |
| SSL \_ CK \_ des \_ 192 \_ EDE3 \_ CBC \_ avec \_ MD5 <br/> Utilisé uniquement lorsque l’application demande explicitement.<br/> | Oui<br/>                      | SSL 2.0<br/>                            |



 

Les suites de chiffrement suivantes sont prises en charge par le fournisseur Microsoft Schannel, mais ne sont pas activées par défaut :



| Chaîne de la suite de chiffrement                                             | Autorisé par SCH \_ utiliser \_ un \_ chiffrement renforcé | Versions du protocole TLS/SSL                     |
|-----------------------------------------------------------------|-------------------------------------|-----------------------------------------------|
| TLS \_ ECDHE \_ RSA \_ avec \_ AES \_ 256 \_ CBC \_ SHA384 \_ P521<br/>   | Oui<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ avec \_ AES \_ 128 \_ CBC \_ SHA256 \_ P521<br/>   | Oui<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ avec \_ AES \_ 256 \_ CBC \_ SHA \_ P521<br/>      | Oui<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ avec \_ AES \_ 128 \_ CBC \_ SHA \_ P521<br/>      | Oui<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ avec \_ AES \_ 256 \_ GCM \_ SHA384 \_ P521<br/> | Oui<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ avec \_ AES \_ 128 \_ GCM \_ SHA256 \_ P521<br/> | Oui<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ avec \_ AES \_ 256 \_ CBC \_ SHA384 \_ P521<br/> | Oui<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ avec \_ AES \_ 128 \_ CBC \_ SHA256 \_ P521<br/> | Oui<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ avec \_ AES \_ 256 \_ CBC \_ SHA \_ P521<br/>    | Oui<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ avec \_ AES \_ 128 \_ CBC \_ SHA \_ P521<br/>    | Oui<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ RSA \_ avec \_ des \_ CBC \_ SHA<br/>                        | Oui<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ EXPORT1024 \_ avec \_ RC4 \_ 56 \_ SHA<br/>             | Non<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ EXPORT1024 \_ avec \_ des \_ CBC \_ SHA<br/>            | Oui<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| \_Exportation RSA \_ TLS \_ avec \_ RC4 \_ 40 \_ MD5<br/>                 | Non<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ avec \_ \_ MD5 null<br/>                            | Oui<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ dhe \_ DSS \_ avec \_ des \_ CBC \_ SHA<br/>                   | Oui<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ dhe \_ DSS \_ EXPORT1024 \_ avec \_ des \_ CBC \_ SHA<br/>       | Oui<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| SSL \_ CK \_ des \_ 64 \_ CBC \_ avec \_ MD5<br/>                     | Oui<br/>                      | SSL 2.0<br/>                            |
| SSL \_ CK \_ RC4 \_ 128 \_ EXPORT40 \_ avec \_ MD5<br/>               | Non<br/>                       | SSL 2.0<br/>                            |



 

Pour ajouter des suites de chiffrement, utilisez l’option stratégie de groupe de la suite de chiffrement SSL sous Configuration ordinateur > Modèles d’administration > paramètres de configuration réseau > SSL pour configurer une liste de priorités pour toutes les suites de chiffrement que vous souhaitez activer.

 

 
