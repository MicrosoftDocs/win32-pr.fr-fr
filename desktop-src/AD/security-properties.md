---
title: Attributs de sécurité utilisateur
description: En plus des propriétés d’attribution de noms pour les objets utilisateur (par exemple, objectGUID, objectSid, CN, distinguishedName, etc.), il existe d’autres propriétés de sécurité utilisées pour l’ouverture de session, l’accès au réseau et le contrôle d’accès.
ms.assetid: eeb16938-4380-4622-804f-6b2ff19aa68d
ms.tgt_platform: multiple
keywords:
- Attributs de sécurité, à l’aide d’AD
- Attributs de sécurité utilisateur Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dfe23252002f2ffbbba3f8e8a8faf5a2d36ce348bdbd7503c0d99a816a81902
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024887"
---
# <a name="user-security-attributes"></a>Attributs de sécurité utilisateur

En plus des propriétés d’attribution de noms pour les objets utilisateur (par exemple, [**objectGUID**](/windows/desktop/ADSchema/a-objectguid), [**objectSID**](/windows/desktop/ADSchema/a-objectsid), [**CN**](/windows/desktop/ADSchema/a-cn), [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname), etc.), il existe d’autres propriétés de sécurité utilisées pour l’ouverture de session, l’accès au réseau et le contrôle d’accès. ces propriétés sont utilisées par le système de sécurité Windows 2000. Ces propriétés peuvent être affichées et gérées par le composant logiciel enfichable utilisateurs et ordinateurs Active Directory.

<dl> <dt>

<span id="accountExpires"></span><span id="accountexpires"></span><span id="ACCOUNTEXPIRES"></span>[**AccountExpires dans**](/windows/desktop/ADSchema/a-accountexpires)
</dt> <dd>

L’attribut [**AccountExpires dans**](/windows/desktop/ADSchema/a-accountexpires) spécifie la date d’expiration d’un compte. Cette valeur est stockée sous la forme d’un grand entier qui représente le nombre d’intervalles de 100 nanosecondes depuis le 1er janvier 1601 (UTC). La valeur **TIMEQ \_ Forever** (définie dans Lmaccess. h) indique qu’un compte n’expire jamais.

</dd> <dt>

<span id="altSecurityIdentities"></span><span id="altsecurityidentities"></span><span id="ALTSECURITYIDENTITIES"></span>[**altSecurityIdentities**](/windows/desktop/ADSchema/a-altsecurityidentities)
</dt> <dd>

L’attribut [**altSecurityIdentities**](/windows/desktop/ADSchema/a-altsecurityidentities) est un attribut à valeurs multiples qui contient des mappages pour les certificats X. 509 ou des comptes d’utilisateur Kerberos externes à cet utilisateur à des fins d’authentification. divers packages de sécurité, y compris le package d’authentification de clé publique et Kerberos, utilisent ces données pour authentifier les utilisateurs lorsqu’ils présentent la forme alternative d’identification, par exemple certificat, UNIX ticket Kerberos, etc. générez un jeton Windows 2000 basé sur le compte d’utilisateur correspondant pour qu’il puisse accéder aux ressources système.

Pour les certificats X. 509, les valeurs doivent correspondre à l’émetteur et aux noms d’objet dans les certificats 509v3, émis par une autorité de certification publique externe, qui mappent au compte d’utilisateur utilisé pour trouver un compte pour l’authentification. Le package SSL (SChannel) utilise la syntaxe suivante : x509 : <somecertinfotype> somecertinfo. Par exemple, la valeur suivante spécifie le nom unique de l’émetteur « \<I\> » avec le DN « C = US, O = InternetCA, CN = APublicCertificateAuthority » et le nom unique du sujet « \<S\> » avec le DN « C = US, O = Fabrikam, ou = sales, CN = Jeff Smith ».


```C++
X509:<I>C=US,O=InternetCA,CN=APublicCertificateAuthority<S>C=US,O=Fabrikam,OU=Sales,CN=Jeff Smith
```



Sachez que « \<S\> » ou « » \<I> et « » \<S\> sont pris en charge. Le fait d’avoir uniquement « \<I\> » n’est pas pris en charge. Les applications ne doivent pas modifier les valeurs dans « \<I\> » ou «» \<S\> , car la correspondance de DN partielle n’est pas prise en charge.

Pour les comptes Kerberos externes, les valeurs doivent être le nom du compte Kerberos. Le package Kerberos utilise la syntaxe suivante : « Kerberos : MITaccountname ». Par exemple, voici la valeur d’un compte sur Fabrikam.com :


```C++
Kerberos:Jeff.Smith@Fabrikam.com
```



</dd> <dt>

<span id="badPasswordTime"></span><span id="badpasswordtime"></span><span id="BADPASSWORDTIME"></span>[**badPasswordTime**](/windows/desktop/ADSchema/a-badpasswordtime)
</dt> <dd>

Non répliqué. L’attribut [**badPasswordTime**](/windows/desktop/ADSchema/a-badpasswordtime) spécifie la dernière fois que l’utilisateur a tenté de se connecter au compte à l’aide d’un mot de passe incorrect. Cette valeur est stockée sous la forme d’un grand entier qui représente le nombre d’intervalles de 100 nanosecondes depuis le 1er janvier 1601 (UTC). Cet attribut est conservé séparément sur chaque contrôleur de domaine du domaine. La valeur zéro signifie que le dernier mot de passe incorrect est inconnu. Pour obtenir une valeur précise pour le dernier mot de passe incorrect de l’utilisateur dans le domaine, chaque contrôleur de domaine dans le domaine doit être interrogé et la valeur la plus élevée doit être utilisée.

</dd> <dt>

<span id="badPwdCount"></span><span id="badpwdcount"></span><span id="BADPWDCOUNT"></span>[**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount)
</dt> <dd>

Non répliqué. L’attribut [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount) spécifie le nombre de fois où l’utilisateur a tenté de se connecter au compte à l’aide d’un mot de passe incorrect. Cet attribut est conservé séparément sur chaque contrôleur de domaine du domaine. La valeur 0 indique que la valeur est inconnue. Pour obtenir une valeur précise pour le nombre total de tentatives de mot de passe incorrectes de l’utilisateur dans le domaine, chaque contrôleur de domaine dans le domaine doit être interrogé et la somme des valeurs doit être utilisée.

</dd> <dt>

<span id="codePage"></span><span id="codepage"></span><span id="CODEPAGE"></span>[**Courante**](/windows/desktop/ADSchema/a-codepage)
</dt> <dd>

L’attribut [**codepage**](/windows/desktop/ADSchema/a-codepage) spécifie la page de codes pour la langue choisie par l’utilisateur. cette valeur n’est pas utilisée par Windows 2000.

</dd> <dt>

<span id="countryCode"></span><span id="countrycode"></span><span id="COUNTRYCODE"></span>[**countryCode**](/windows/desktop/ADSchema/a-countrycode)
</dt> <dd>

L’attribut [**CountryCode**](/windows/desktop/ADSchema/a-countrycode) spécifie le code de pays/région pour la langue de l’utilisateur. cette valeur n’est pas utilisée par Windows 2000.

</dd> <dt>

<span id="homeDirectory"></span><span id="homedirectory"></span><span id="HOMEDIRECTORY"></span>[**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory)
</dt> <dd>

L’attribut [**HomeDirectory**](/windows/desktop/ADSchema/a-homedirectory) spécifie le chemin d’accès du répertoire de démarrage de l’utilisateur. La chaîne peut être null.

Si [**le**](/windows/desktop/ADSchema/a-homedrive) lecteur de disque est défini et spécifie une lettre de lecteur, [**HomeDirectory**](/windows/desktop/ADSchema/a-homedirectory) doit être un chemin d’accès UNC. Le chemin d’accès doit être un chemin d’accès UNC réseau au format \\ \\ Répertoire de partage du serveur \\ \\ . Cette valeur peut être une chaîne NULL.

Si le paramètre [**homeDrive**](/windows/desktop/ADSchema/a-homedrive) n’est pas défini, [**HomeDirectory**](/windows/desktop/ADSchema/a-homedirectory) doit être un chemin d’accès local, par exemple, C : \\ mylocaldir.

</dd> <dt>

<span id="homeDrive"></span><span id="homedrive"></span><span id="HOMEDRIVE"></span>[**homeDrive**](/windows/desktop/ADSchema/a-homedrive)
</dt> <dd>

L’attribut [**homeDrive**](/windows/desktop/ADSchema/a-homedrive) spécifie la lettre de lecteur à laquelle mapper le chemin UNC spécifié par **HomeDirectory**. La lettre de lecteur doit être spécifiée sous la forme suivante :


```C++
<drive letter>:
```



où « \<drive letter\> » correspond à la lettre du lecteur à mapper. Par exemple :


```C++
Z:
```



Si cet attribut n’est pas défini, [**HomeDirectory**](/windows/desktop/ADSchema/a-homedirectory) doit être un chemin d’accès local, par exemple, C : \\ mylocaldir.

</dd> <dt>

<span id="lastLogoff"></span><span id="lastlogoff"></span><span id="LASTLOGOFF"></span>[**lastLogoff**](/windows/desktop/ADSchema/a-lastlogoff)
</dt> <dd>

Non répliqué. L’attribut [**lastLogoff**](/windows/desktop/ADSchema/a-lastlogoff) spécifie à quel moment la dernière déconnexion s’est produite. Cette valeur est stockée sous la forme d’un grand entier qui représente le nombre d’intervalles de 100 nanosecondes depuis le 1er janvier 1601 (UTC). La partie haute de ce grand entier correspond au membre **dwHighDateTime** de la structure [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) et la partie inférieure correspond au membre **dwLowDateTime** de la structure **fileTime** . Cet attribut est conservé séparément sur chaque contrôleur de domaine du domaine. La valeur zéro signifie que la dernière heure de déconnexion est inconnue. Pour obtenir une valeur précise pour la dernière fermeture de session de l’utilisateur dans le domaine, chaque contrôleur de domaine dans le domaine doit être interrogé et la valeur la plus élevée doit être utilisée.

</dd> <dt>

<span id="lastLogon"></span><span id="lastlogon"></span><span id="LASTLOGON"></span>[**lastLogon**](/windows/desktop/ADSchema/a-lastlogon)
</dt> <dd>

Non répliqué. L’attribut [**lastLogon**](/windows/desktop/ADSchema/a-lastlogon) spécifie à quel moment la dernière ouverture de session s’est produite. Cette valeur est stockée sous la forme d’un grand entier qui représente le nombre d’intervalles de 100 nanosecondes depuis le 1er janvier 1601 (UTC). La partie haute de ce grand entier correspond au membre **dwHighDateTime** de la structure [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) et la partie inférieure correspond au membre **dwLowDateTime** de la structure **fileTime** . Cet attribut est conservé séparément sur chaque contrôleur de domaine du domaine. La valeur zéro signifie que l’heure de la dernière connexion est inconnue. Pour obtenir une valeur précise pour la dernière ouverture de session de l’utilisateur dans le domaine, chaque contrôleur de domaine dans le domaine doit être interrogé et la valeur la plus élevée doit être utilisée.

</dd> <dt>

<span id="lmPwdHistory"></span><span id="lmpwdhistory"></span><span id="LMPWDHISTORY"></span>[**lmPwdHistory**](/windows/desktop/ADSchema/a-lmpwdhistory)
</dt> <dd>

L’attribut [**lmPwdHistory**](/windows/desktop/ADSchema/a-lmpwdhistory) est l’historique des mots de passe de l’utilisateur dans le format à sens unique (OWF) LAN Manager (LM). LM avec LM est utilisé pour la compatibilité avec les clients LAN Manager 2. x, Windows 95 et Windows 98. Cet attribut est utilisé uniquement par le système d’exploitation. N’oubliez pas que vous ne pouvez pas dériver le mot de passe en texte clair de la forme OWF du mot de passe.

</dd> <dt>

<span id="logonCount"></span><span id="logoncount"></span><span id="LOGONCOUNT"></span>[**logonCount**](/windows/desktop/ADSchema/a-logoncount)
</dt> <dd>

Non répliqué. L’attribut [**logonCount**](/windows/desktop/ADSchema/a-logoncount) compte le nombre de fois où l’utilisateur a réussi à se connecter à ce compte. Cet attribut est conservé sur chaque contrôleur de domaine du domaine. La valeur 0 indique que la valeur est inconnue. Pour obtenir une valeur précise pour le nombre total de tentatives de connexion réussies de l’utilisateur dans le domaine, chaque contrôleur de domaine dans le domaine doit être interrogé et la somme des valeurs doit être utilisée.

</dd> <dt>

<span id="mail"></span><span id="MAIL"></span>[**messagerie**](/windows/desktop/ADSchema/a-mail)
</dt> <dd>

L’attribut [**mail**](/windows/desktop/ADSchema/a-mail) est un attribut à valeur unique qui contient l’adresse SMTP de l’utilisateur, par exemple, « jeff@Fabrikam.com ».

</dd> <dt>

<span id="maxStorage"></span><span id="maxstorage"></span><span id="MAXSTORAGE"></span>[**maxStorage**](/windows/desktop/ADSchema/a-maxstorage)
</dt> <dd>

L’attribut [**maxStorage**](/windows/desktop/ADSchema/a-maxstorage) spécifie la quantité maximale d’espace disponible sur le disque dur que l’utilisateur peut utiliser. Utilisez la valeur **User \_ MAXSTORAGE \_ Unlimited** (définie dans Lmaccess. h) pour utiliser tout l’espace disque disponible.

</dd> <dt>

<span id="memberOf"></span><span id="memberof"></span><span id="MEMBEROF"></span>[**memberOf**](/windows/desktop/ADSchema/a-memberof)
</dt> <dd>

L’attribut [**memberOf**](/windows/desktop/ADSchema/a-memberof) est un attribut à valeurs multiples qui contient des groupes dont l’utilisateur est un membre direct, à l’exception du groupe principal, représenté par [**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid). L’appartenance au groupe dépend du contrôleur de domaine (DC) à partir duquel cet attribut est récupéré :

-   Sur un contrôleur de domaine pour le domaine qui contient l’utilisateur, [**memberOf**](/windows/desktop/ADSchema/a-memberof) pour l’utilisateur est terminé en ce qui concerne l’appartenance aux groupes de ce domaine. Toutefois, **memberOf** ne contient pas l’appartenance de l’utilisateur aux groupes locaux et globaux de domaine dans d’autres domaines.
-   Sur un serveur de catalogue global, [**memberOf**](/windows/desktop/ADSchema/a-memberof) pour l’utilisateur est complet par rapport à toutes les appartenances aux groupes universels.

Si les deux conditions sont vraies pour le DC, les deux jeux de données sont contenus dans [**memberOf**](/windows/desktop/ADSchema/a-memberof).

N’oubliez pas que cet attribut répertorie les groupes qui contiennent l’utilisateur dans leur attribut de membre ; il ne contient pas la liste récursive des prédécesseurs imbriqués. Par exemple, si l’utilisateur O est membre du groupe C et que le groupe b a été imbriqué dans le groupe A, l’attribut [**memberOf**](/windows/desktop/ADSchema/a-memberof) de l’utilisateur O listerait le groupe C et le groupe b, mais pas le groupe a.

Cet attribut n’est pas stocké, il s’agit d’un attribut de lien arrière calculé.

</dd> <dt>

<span id="ntPwdHistory"></span><span id="ntpwdhistory"></span><span id="NTPWDHISTORY"></span>[**ntPwdHistory**](/windows/desktop/ADSchema/a-ntpwdhistory)
</dt> <dd>

L’attribut [**ntPwdHistory**](/windows/desktop/ADSchema/a-ntpwdhistory) est l’historique des mots de passe de l’utilisateur dans Windows format à sens unique NT (OWF). Windows 2000 utilise le Windows NT OWF. Cet attribut est utilisé uniquement par le système d’exploitation. N’oubliez pas que vous ne pouvez pas dériver le mot de passe en texte clair de la forme OWF du mot de passe.

</dd> <dt>

<span id="otherMailbox"></span><span id="othermailbox"></span><span id="OTHERMAILBOX"></span>[**otherMailbox**](/windows/desktop/ADSchema/a-othermailbox)
</dt> <dd>

L’attribut [**otherMailbox**](/windows/desktop/ADSchema/a-othermailbox) est un attribut à valeurs multiples qui contient d’autres adresses de messagerie supplémentaires dans un formulaire, par exemple, « CCMAIL : JeffSmith ».

</dd> <dt>

<span id="PasswordExpirationDate"></span><span id="passwordexpirationdate"></span><span id="PASSWORDEXPIRATIONDATE"></span>[**PasswordExpirationDate**](/windows/desktop/ADSI/iadsuser-property-methods)
</dt> <dd>

La date d’expiration du mot de passe n’est pas un attribut de l’objet utilisateur. Il s’agit d’une valeur calculée en fonction de la somme de [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset) pour l’utilisateur et [**maxPwdAge**](/windows/desktop/ADSchema/a-maxpwdage) du domaine de l’utilisateur. Pour connaître la date d’expiration du mot de passe, récupérez la propriété [**IADsUser. PasswordExpirationDate**](/windows/desktop/ADSI/iadsuser-property-methods) . Vous ne pouvez pas modifier cet attribut pour un utilisateur ; au lieu de cela, définissez la propriété [**IADsDomain. MaxPasswordAge**](/windows/desktop/ADSI/iadsdomain-property-methods) pour modifier le paramètre du domaine.

</dd> <dt>

<span id="primaryGroupID"></span><span id="primarygroupid"></span><span id="PRIMARYGROUPID"></span>[**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid)
</dt> <dd>

L’attribut [**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid) est un attribut à valeur unique qui contient le [**primaryGroupToken**](/windows/desktop/ADSchema/a-primarygrouptoken) du groupe qui est le groupe principal de l’objet. Le groupe principal de l’objet n’est pas inclus dans l’attribut [**memberOf**](/windows/desktop/ADSchema/a-memberof) . Par exemple, par défaut, le groupe principal d’un objet utilisateur est le **primaryGroupToken** du groupe utilisateurs du domaine, mais le groupe utilisateurs du domaine ne fait pas partie de l’attribut **memberOf** de l’objet utilisateur.

</dd> <dt>

<span id="profilePath"></span><span id="profilepath"></span><span id="PROFILEPATH"></span>[**profilePath**](/windows/desktop/ADSchema/a-profilepath)
</dt> <dd>

L’attribut [**profilePath**](/windows/desktop/ADSchema/a-profilepath) spécifie un chemin d’accès au profil de l’utilisateur. Cette valeur peut être une chaîne NULL, un chemin d’accès absolu local ou un chemin d’accès UNC.

</dd> <dt>

<span id="pwdLastSet"></span><span id="pwdlastset"></span><span id="PWDLASTSET"></span>[**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset)
</dt> <dd>

L’attribut [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset) spécifie le moment auquel le mot de passe a été modifié pour la dernière fois. Cette valeur est stockée sous la forme d’un grand entier qui représente le nombre d’intervalles de 100 nanosecondes depuis le 1er janvier 1601 (UTC).

Le système utilise la valeur de cet attribut et l’attribut [**maxPwdAge**](/windows/desktop/ADSchema/a-maxpwdage) du domaine qui contient l’objet utilisateur pour calculer la date d’expiration du mot de passe. Autrement dit, la somme de [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset) pour l’utilisateur et **maxPwdAge** du domaine de l’utilisateur.

Cet attribut détermine si l’utilisateur doit modifier le mot de passe lorsque l’utilisateur se connecte ensuite. Si [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset) est égal à zéro, la valeur par défaut, l’utilisateur doit modifier le mot de passe à la prochaine ouverture de session. La valeur-1 indique que l’utilisateur n’a pas besoin de modifier le mot de passe à la prochaine ouverture de session. Le système définit cette valeur sur-1 après que l’utilisateur a défini le mot de passe.

</dd> <dt>

<span id="sAMAccountType"></span><span id="samaccounttype"></span><span id="SAMACCOUNTTYPE"></span>[**sAMAccountType**](/windows/desktop/ADSchema/a-samaccounttype)
</dt> <dd>

L’attribut [**samAccountType**](/windows/desktop/ADSchema/a-samaccounttype) spécifie un entier qui représente le type de compte. Cela est défini par le système d’exploitation lors de la création de l’objet.

</dd> <dt>

<span id="scriptPath"></span><span id="scriptpath"></span><span id="SCRIPTPATH"></span>[**scriptPath**](/windows/desktop/ADSchema/a-scriptpath)
</dt> <dd>

L’attribut [**ScriptPath**](/windows/desktop/ADSchema/a-scriptpath) spécifie le chemin d’accès du fichier de script d’ouverture de session,. cmd, .exe ou .bat de l’utilisateur. La chaîne peut être null.

</dd> <dt>

<span id="unicodePwd"></span><span id="unicodepwd"></span><span id="UNICODEPWD"></span>[**unicodePwd**](/windows/desktop/ADSchema/a-unicodepwd)
</dt> <dd>

L’attribut [**unicodePwd**](/windows/desktop/ADSchema/a-unicodepwd) est le mot de passe de l’utilisateur.

Pour définir le mot de passe de l’utilisateur, utilisez la méthode [**IADsUser. ChangePassword**](/windows/desktop/api/iads/nf-iads-iadsuser-changepassword) , si votre script ou application permet à l’utilisateur de modifier son propre mot de passe, ou la méthode [**IADsUser. SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) , si votre script ou votre application autorise un administrateur à réinitialiser un mot de passe.

Mot de passe de l’utilisateur dans Windows format à sens unique NT (OWF). Windows 2000 utilise le Windows NT OWF. Cet attribut est utilisé uniquement par le système d’exploitation. N’oubliez pas que vous ne pouvez pas dériver le mot de passe en texte clair de la forme OWF du mot de passe.

</dd> <dt>

<span id="userAccountControl"></span><span id="useraccountcontrol"></span><span id="USERACCOUNTCONTROL"></span>[**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol)
</dt> <dd>

L’attribut [**UserAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) spécifie des indicateurs qui contrôlent le mot de passe, le verrouillage, la désactivation, l’activation, le script et le comportement du répertoire de démarrage pour l’utilisateur. Cet attribut contient également un indicateur qui indique le type de compte de l’objet. L’objet utilisateur a généralement le \_ compte standard UF \_ défini.

Les indicateurs suivants sont définis dans Lmaccess. h.



| Indicateur                     | Description                                                                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_script uf               | Le script d’ouverture de session a été exécuté. Cette valeur doit être définie pour LAN Manager 2,0 ou Windows NT.                                                                             |
| \_ACCOUNTDISABLE uf       | Le compte d’utilisateur est désactivé.                                                                                                                                    |
| UF \_ homedir \_ requis    | Le répertoire de départ est requis. cette valeur est ignorée dans Windows NT et Windows 2000.                                                                            |
| \_NOTREQD passwd passwd \_      | Aucun mot de passe n'est requis.                                                                                                                                         |
| modification de la \_ \_ décantation de passwd UF \_ | L’utilisateur ne peut pas modifier le mot de passe.                                                                                                                             |
| \_verrouillage uf              | Le compte est actuellement verrouillé. Cette valeur peut être désactivée pour déverrouiller un compte précédemment verrouillé. Cette valeur ne peut pas être utilisée pour verrouiller un compte précédemment verrouillé. |
| UF ne pas faire \_ \_ expirer \_ passwd | Représente le mot de passe, qui ne doit jamais expirer sur le compte.                                                                                               |



 

Les indicateurs suivants décrivent le type de compte. Une seule valeur peut être définie. Vous ne pouvez pas modifier le type de compte.



| Indicateur                            | Description                                                                                                                                                                                                                                     |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_compte standard \_ uf             | Il s’agit d’un type de compte par défaut qui représente un utilisateur standard.                                                                                                                                                                                  |
| \_ \_ compte DUPLIQUÉ temporaire \_ uf    | Il s’agit d’un compte pour les utilisateurs dont le compte principal se trouve dans un autre domaine. Ce compte fournit l’accès utilisateur à ce domaine, mais pas à un domaine qui approuve ce domaine. Le gestionnaire de l’utilisateur fait référence à ce type de compte en tant que compte d’utilisateur local. |
| compte d’approbation de station de \_ travail UF \_ \_ | il s’agit d’un compte d’ordinateur pour un serveur Windows nt Workstation/Windows 2000 Professional ou Windows nt server/Windows 2000 qui est membre de ce domaine.                                                                                     |
| \_compte de \_ confiance du serveur uf \_      | Il s’agit d’un compte d’ordinateur pour un contrôleur de domaine de sauvegarde Windows NT qui est membre de ce domaine.                                                                                                                                           |
| \_compte de confiance interdomaine UF \_ \_ | Il s’agit d’un permis de faire confiance au compte d’un domaine NT Windows qui approuve d’autres domaines.                                                                                                                                                            |



 

</dd> <dt>

<span id="userCertificate"></span><span id="usercertificate"></span><span id="USERCERTIFICATE"></span>[**userCertificate**](/windows/desktop/ADSchema/a-usercertificate)
</dt> <dd>

L’attribut [**userCertificate**](/windows/desktop/ADSchema/a-usercertificate) est un attribut à valeurs multiples qui contient les certificats X509v3 encodés der émis à l’utilisateur. N’oubliez pas que cet attribut contient les certificats de clé publique émis à cet utilisateur par le service de certificats Microsoft.

</dd> <dt>

<span id="userSharedFolder"></span><span id="usersharedfolder"></span><span id="USERSHAREDFOLDER"></span>[**userSharedFolder**](/windows/desktop/ADSchema/a-usersharedfolder)
</dt> <dd>

L’attribut [**userSharedFolder**](/windows/desktop/ADSchema/a-usersharedfolder) spécifie un chemin d’accès UNC au dossier Documents partagés de l’utilisateur. Le chemin d’accès doit être un chemin d’accès UNC réseau au format \\ \\ Répertoire de partage du serveur \\ \\ . Cette valeur peut être une chaîne NULL.

</dd> <dt>

<span id="userWorkstations"></span><span id="userworkstations"></span><span id="USERWORKSTATIONS"></span>[**userWorkstations**](/windows/desktop/ADSchema/a-userworkstations)
</dt> <dd>

L’attribut [**userWorkstations**](/windows/desktop/ADSchema/a-userworkstations) est un attribut à valeur unique qui contient les noms NetBIOS des stations de travail à partir desquelles l’utilisateur peut se connecter. Chaque nom NetBIOS est séparé par une virgule.

Si aucune valeur n’est définie, cela indique qu’il n’existe aucune restriction. Pour désactiver les ouvertures de session de toutes les stations de travail de ce compte, définissez la \_ valeur UF ACCOUNTDISABLE (définie dans Lmaccess. h) dans l’attribut [**UserAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) .

</dd> </dl>

 

 
