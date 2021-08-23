---
title: Authentification (BITS)
description: BITS prend en charge l’authentification de base, l’authentification Passport et plusieurs schémas d’authentification stimulation/réponse.
ms.assetid: cfd4aec3-79d0-4971-93f8-df797e5c0f75
ms.topic: article
ms.date: 10/09/2018
ms.openlocfilehash: 9cb3d50f6689ed28889c68388969c1cb7d06ea912bc5d5ed4384f45a4e740f79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021287"
---
# <a name="authentication-bits"></a>Authentification (BITS)

BITS prend en charge l’authentification de base, l’authentification Passport et plusieurs schémas d’authentification stimulation/réponse. Si le serveur ou le proxy requiert l’authentification de l’utilisateur, utilisez la fonction [**IBackgroundCopyJob2 :: SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) pour spécifier les informations d’identification de l’utilisateur. Le service BITS utilise le [CryptoAPI](/windows/desktop/SecCrypto/cryptography-portal) pour protéger les informations d’identification.

Pour définir les informations d’identification pour l’authentification de base, utilisez la fonction [**SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) pour spécifier le nom d’utilisateur et le mot de passe. Vous devez uniquement utiliser l’authentification de base avec des sites Web sécurisés protégés par https://; dans le cas contraire, le nom d’utilisateur et le mot de passe seront visibles pour les utilisateurs. 

Il est possible d’incorporer le nom d’utilisateur et le mot de passe dans l’URL. Cela n’est pas considéré comme une bonne pratique de sécurité et est déconseillé dans le document RFC 3986 (section 3.2.1).

Pour l’authentification [Passport](/windows/desktop/WinHttp/passport-authentication-in-winhttp) , bits prend en charge uniquement les informations d’identification explicites, pas les informations d’identification implicites liées au compte.

Pour l’authentification par stimulation/réponse, le service BITS emprunte l’identité de l’utilisateur et utilise [Snego](../com/snego.md) pour déterminer l’authentification par stimulation/réponse à utiliser, comme NTLM ou le protocole Kerberos. Pour obtenir la liste des schémas de stimulation/réponse pris en charge par BITS, consultez [**\_ \_ schéma d’authentification BG**](/windows/desktop/api/Bits1_5/ne-bits1_5-bg_auth_scheme).

Les tâches BITS peuvent échouer si le répertoire virtuel sur le serveur a une authentification anonyme et qu’un autre schéma d’authentification est activé et que les listes de contrôle d’accès protègent le répertoire virtuel ou téléchargent les fichiers. Par exemple, un travail échoue avec « accès refusé » si l’authentification anonyme et l’authentification intégrée du répertoire virtuel sont activées et si le fichier contient une liste de contrôle d’accès qui autorise uniquement Ben à lire le fichier. Cela est dû au fait que le répertoire virtuel autorise l’accès anonyme. par conséquent, IIS n’authentifie pas explicitement Ben (les informations d’identification de l’Olivier ne sont pas utilisées pour accéder au fichier et l’accès est refusé).

## <a name="using-implicit-credentials"></a>Utilisation d’informations d’identification implicites

Pour utiliser les informations d’identification implicites (Logon) de l’utilisateur pour l’authentification NTLM ou Kerberos, appelez la méthode [**IBackgroundCopyJob2 :: SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) et définissez les membres **nom d’utilisateur** et **mot de passe** de la structure des [**\_ \_ informations d’identification de base BG**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_basic_credentials) sur la **valeur null**. Si vous spécifiez des informations d’identification implicites pour un proxy, BITS utilise également les informations d’identification implicites pour l’authentification du serveur, sauf si vous spécifiez des informations d’identification de serveur explicites.

Pour plus d’informations sur les services, consultez [comptes de service et bits](service-accounts-and-bits.md).

Vous pouvez également modifier la valeur de Registre **LmCompatibilityLevel** ou **UseLMCompat** . Toutefois, vous ne devez modifier ces valeurs que si vous disposez d’une application existante qui ne peut pas être modifiée pour appeler la méthode [**SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) .

BITS utilisera des informations d’identification implicites pour l’authentification si la valeur de Registre **LmCompatibilityLevel** est supérieure ou égale à deux, et que vous n’avez pas appelé la méthode [**SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) . Le chemin d’accès complet à la valeur de Registre **LmCompatibilityLevel** est **HKEY \_ local \_ machine** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **LSA** \\ **LmCompatibilityLevel**.

Notez que la modification de la valeur de Registre **LmCompatibilityLevel** peut affecter les autres applications et services exécutés sur l’ordinateur. Pour plus d’informations sur l’utilisation de la valeur de Registre **LmCompatibilityLevel** , consultez [KB147706](https://support.microsoft.com/kb/147706).

si la définition de la valeur de registre **LMCompatibilityLevel** est un problème, vous pouvez créer la valeur de registre **UseLMCompat** sous **HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **BITS**. La valeur de Registre est un DWORD. Le tableau suivant répertorie les valeurs possibles pour **UseLMCompat**:

|Valeur|Description|
|-|-|
| 0     | BITS enverra des informations d’identification implicites chaque fois que le serveur demande des informations d’identification NTLM ou Kerberos.                                                                                           |
| 1     | BITS enverra des informations d’identification implicites uniquement si la valeur de Registre **LmCompatibilityLevel** de l’ordinateur client est supérieure ou égale à 2.<br/>     |
| 2     | BITS enverra des informations d’identification implicites uniquement si l’application a appelé la méthode [**SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) .<br/> |

Le service BITS utilise la valeur par défaut « 2 » pour la valeur de Registre **UseLMCompat** si la valeur de Registre n’existe pas.

## <a name="using-certificates-for-clientserver-authentication"></a>Utilisation de certificats pour l’authentification client/serveur

Dans une communication sécurisée de client/serveur, les clients et les serveurs peuvent utiliser des certificats numériques pour s’authentifier mutuellement. BITS prend automatiquement en charge l’authentification du serveur basée sur des certificats pour les transports HTTP sécurisés. Pour fournir à BITS le certificat client nécessaire pour l’authentification mutuelle, appelez la méthode [**IBackgroundCopyJobHttpOptions :: SetClientCertificateByID**](/windows/desktop/api/Bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setclientcertificatebyid) ou [**IBackgroundCopyJobHttpOptions :: SetClientCertificateByName**](/windows/desktop/api/Bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setclientcertificatebyname) .

Lorsqu’un site Web accepte, mais ne nécessite pas de certificat client SSL, et que le travail BITS ne spécifie pas de certificat client, le travail échoue avec le certificat d' **\_ authentification du \_ client WinHTTP \_ \_ \_ nécessaire** (0x80072f0c).

## <a name="how-to-handle-authenticated-proxy-scenarios-that-require-user-specific-settings"></a>Comment gérer les scénarios de proxy authentifiés qui requièrent des paramètres spécifiques à l’utilisateur

Si vous utilisez BITS dans un environnement qui requiert l’authentification du proxy lors de l’exécution en tant que compte sans informations d’identification NTLM ou Kerberos utilisables dans le domaine réseau de l’ordinateur, vous devez effectuer des étapes supplémentaires pour vous authentifier correctement à l’aide des informations d’identification d’un autre compte d’utilisateur qui possède des informations d’identification sur le domaine. Il s’agit d’un scénario classique dans lequel votre code BITS s’exécute en tant que service système tel que LocalService, NetworkService ou LocalSystem, car ces comptes n’ont pas d’informations d’identification NTLM ou Kerberos utilisables.

La logique de détection de proxy utilisée dans le service BITS effectue les opérations suivantes lorsqu’un jeton d’assistance réseau ( \_ réseau de jetons BG \_ ) est défini :

-   Si [**méthode ibackgroundcopyjob :: setproxysettings n'**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) a été appelé avec la **\_ \_ \_ \_ préconfiguration de l’utilisation du proxy de tâche BG**, lisez les paramètres du proxy IE local à l’aide de l’emprunt d’identité du contexte de jeton de propriétaire de tâche via [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser). à partir de Windows 10, version 1809 (10,0 ; Build 17763), l’identité du jeton d’assistance est utilisée pour cette étape.
-   Si [**méthode ibackgroundcopyjob :: setproxysettings n'**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) a été appelé avec la détection automatique de l' **\_ utilisation du proxy \_ \_ BG** ou si les paramètres IE de la **tâche BG configuration de l’utilisation du proxy de la \_ tâche \_ \_ \_ BG** spécifient la détection automatique ou une URL de configuration automatique, effectuent la détection automatique de proxy ou le protocole WPAD (Web proxy AutoDiscovery Protocol) à [**l’aide de**](/windows/desktop/api/winhttp/nf-winhttp-winhttpgetproxyforurl)l’emprunt d’identité du jeton d’assistance via

Après cela, l’emprunt d’identité du jeton d’assistance est utilisé pour l’authentification du proxy ou du serveur dans.

à partir de Windows 10, version 1809 (10,0 ; Build 17763), le scénario de proxy authentifié avec des informations d’identification spécifiques à l’utilisateur est simplifié.

1.  Appelez la méthode [**SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) de la tâche bits avec le **schéma d' \_ authentification BG \_ \_ Negotiate**, le *nom d’utilisateur* ayant la valeur **null**, le *mot de passe* défini sur **null** et la *cible* sur le **\_ \_ \_ proxy de cible d’authentification BG**. Cela entraîne l’utilisation des informations d’identification implicites du compte d’utilisateur pour l’authentification NTLM et Kerberos avec le proxy et le serveur.
2.  Appelez [**méthode ibackgroundcopyjob :: setproxysettings n'**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) avec **la \_ \_ \_ \_ préconfiguration de l’utilisation du proxy de tâche BG**.
3.  QueryInterface pour [**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions).
4.  Emprunter l’identité du compte d’utilisateur que vous utilisez pour les informations d’identification NTLM/Kerberos.
5.  Appelez [**SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken).
6. Appelez [**SetHelperTokenFlags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) avec **le \_ \_ réseau de jetons BG**.
7. Rétablissez l’emprunt d’identité.
8. Poursuivez la configuration de la tâche.
9. Appelez [**Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) sur le travail.

avant le Windows 10, version 1809 (10,0 ; Build 17763), l’identité de l’utilisateur correcte (identité du jeton d’assistance) est utilisée pour la détection du proxy basé sur le réseau (WPAD) et pour l’authentification du proxy, mais la détection réelle des paramètres du proxy local (IE) est toujours effectuée à l’aide du jeton du propriétaire du travail, même lorsqu’un jeton d’assistance est configuré. Pour contourner ce manque, vous pouvez suivre ces étapes.

1.  Emprunter l’identité du compte d’utilisateur que vous utilisez pour les informations d’identification NTLM/Kerberos.
2.  Récupérez les paramètres du proxy IE du compte d’utilisateur en appelant [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser).
3.  Rétablissez l’emprunt d’identité.
4.  Appelez la méthode [**SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) de la tâche bits avec le **schéma d' \_ authentification BG \_ \_ Negotiate**, le *nom d’utilisateur* ayant la valeur **null**, le *mot de passe* défini sur **null** et la *cible* sur le **\_ \_ \_ proxy de cible d’authentification BG**. Cela entraîne l’utilisation des informations d’identification implicites du compte d’utilisateur pour l’authentification NTLM et Kerberos avec le proxy et le serveur.
5.  Si l’étape 2 a généré des paramètres de proxy spécifiques à l’utilisateur (par exemple, *lpszProxy* ou *lpszProxyBypass* n’ont pas la **valeur null**), définissez manuellement les paramètres de travail correspondants à l’aide de [**setproxysettings n'**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) avec le paramètre de **\_ \_ \_ \_ remplacement utilisation du proxy de tâche BG** .
6.  Si l’étape 2 n’a pas produit de paramètres de proxy spécifiques à l’utilisateur, appelez [**setproxysettings n'**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) avec la **\_ \_ \_ préconfiguration de l’utilisation du travail BG**.
7.  QueryInterface pour [**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions).
8.  Emprunter à nouveau le compte d’utilisateur.
9.  Appelez [**SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken).
10. Appelez [**SetHelperTokenFlags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) avec **le \_ \_ réseau de jetons BG**.
11. Rétablissez l’emprunt d’identité.
12. Poursuivez la configuration de la tâche.
13. Appelez [**Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) sur le travail.
