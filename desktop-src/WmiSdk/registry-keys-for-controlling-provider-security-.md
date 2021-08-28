---
description: pour améliorer la sécurité du processus hôte du fournisseur partagé (wmiprvse.exe) Windows Management Instrumentation (WMI), des modifications ont été apportées aux plateformes Windows qui sécurisent le processus hôte du fournisseur à l’aide d’un identificateur de sécurité (SID) de service.
ms.assetid: f93ac155-512c-4efa-8168-ca2d56fe6f01
ms.tgt_platform: multiple
title: Clés et valeurs de Registre pour le contrôle de la sécurité du fournisseur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 916a5910a6ad21e9f9dfdcfc0992de10ae30da82
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884360"
---
# <a name="registry-keys-and-values-for-controlling-provider-security"></a>Clés et valeurs de Registre pour le contrôle de la sécurité du fournisseur

pour améliorer la sécurité du processus hôte du fournisseur partagé (wmiprvse.exe) Windows Management Instrumentation (WMI), des modifications ont été apportées aux plateformes Windows qui sécurisent le processus hôte du fournisseur à l’aide d’un [*identificateur de sécurité (SID) de service*](gloss-s.md). Ces modifications introduisent les modes d’exécution suivants pour l’hôte partagé WMI : sécurisé et compatible.

Les sections suivantes sont traitées dans cette rubrique :

-   [Modes sécurisés et compatibles](#secure-and-compatible-modes)
-   [Clés et valeurs de Registre](#registry-keys-and-values)
-   [Configuration d’un fournisseur pour qu’il s’exécute en mode sécurisé ou compatible](#configuring-a-provider-to-run-in-secure-or-compatible-mode)

## <a name="secure-and-compatible-modes"></a>Modes sécurisés et compatibles

à partir de Windows 7, les deux modes d’exécution suivants du processus hôte partagé WMI ont été ajoutés :

<dl> <dt>

<span id="Secure_mode"></span><span id="secure_mode"></span><span id="SECURE_MODE"></span>Mode sécurisé
</dt> <dd>

Les ressources de processus hôte du fournisseur WMI sont sécurisées avec un [*SID de service*](gloss-s.md). Seul le *SID du service* dispose d’autorisations pour ces ressources.

</dd> <dt>

<span id="Compatible_mode"></span><span id="compatible_mode"></span><span id="COMPATIBLE_MODE"></span>Mode compatible
</dt> <dd>

Le processus hôte du fournisseur partagé WMI n’est pas sécurisé avec un [*SID de service*](gloss-s.md). Le processus hôte du fournisseur autorise l’accès aux comptes NetworkService ou LocalService en fonction du modèle d’hébergement. Pour plus d’informations sur les modèles d’hébergement, consultez [hébergement et sécurité du fournisseur](provider-hosting-and-security.md).

</dd> </dl>

**Windows Vista et Windows Server 2008 :** Pour accéder aux clés de Registre et aux valeurs de contrôle des modes sécurisé et compatible pour le processus hôte du fournisseur, vous devez installer la mise à jour de sécurité dans l' [article 959454](https://support.microsoft.com/kb/959454)de la base de connaissances. Pour plus d’informations, consultez le [Bulletin de sécurité Microsoft MS09-012](https://www.microsoft.com/technet/security/bulletin/ms09-012.mspx).

## <a name="registry-keys-and-values"></a>Clés et valeurs de Registre

Les paramètres de mode sécurisé et compatible sont spécifiés via des clés de registre. Les clés de Registre pour WMI se trouvent dans le registre de la clé **HKEY \_ local \_ machine** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ .

Les clés de Registre et la valeur **DWORD** suivantes décrites dans la liste suivante ont été ajoutées pour contrôler le comportement des fournisseurs WMI.

<dl> <dt>

<span id="SecuredHostProviders"></span><span id="securedhostproviders"></span><span id="SECUREDHOSTPROVIDERS"></span>**SecuredHostProviders**
</dt> <dd>

Cette clé contrôle le comportement des fournisseurs individuels. Tous les fournisseurs répertoriés dans cette clé s’exécutent toujours en mode sécurisé. tous les fournisseurs de boîtes de réception fournis avec Windows sont répertoriés sous cette clé et sont exécutés en mode sécurisé par défaut.

Cette clé est prioritaire sur les fournisseurs listés dans la clé **CompatibleHostProviders** .

</dd> <dt>

<span id="CompatibleHostProviders"></span><span id="compatiblehostproviders"></span><span id="COMPATIBLEHOSTPROVIDERS"></span>**CompatibleHostProviders**
</dt> <dd>

Cette clé contrôle le comportement des fournisseurs individuels. Tous les fournisseurs répertoriés dans cette clé s’exécutent toujours en mode compatible. Cette clé est vide par défaut.

Si un fournisseur est listé à la fois dans la clé **SecuredHostProviders** et dans la clé **CompatibleHostProviders** , le fournisseur est exécuté en mode sécurisé.

> [!Note]  
> La clé **CompatibleHostProviders** fournit une compatibilité d’application pour les applications tierces si la clé **DefaultSecuredHost** est définie sur 1 et que le fournisseur est connu pour ne pas fonctionner en mode sécurisé.

 

</dd> <dt>

<span id="DefaultSecuredHost"></span><span id="defaultsecuredhost"></span><span id="DEFAULTSECUREDHOST"></span>**DefaultSecuredHost**
</dt> <dd>

Valeur **DWORD** de Registre globale qui détermine si tous les fournisseurs, qui ne sont pas répertoriés dans les clés **SecuredHostProviders** ou **CompatibleHostProviders** , sont exécutés en mode sécurisé ou compatible. Cette valeur **DWORD** permet à l’administrateur de décider du mode d’exécution d’un fournisseur tiers. Par défaut, cette valeur est définie sur zéro et tous les fournisseurs tiers sont exécutés en mode compatible. Les administrateurs peuvent renforcer la sécurité de leur ordinateur par défaut en définissant la valeur **DefaultSecuredHost** sur 1.

> [!Note]  
> La valeur **DefaultSecuredHost** n’affecte pas les autres clés de registre. Les fournisseurs répertoriés dans la clé **SecuredHostProviders** restent en mode sécurisé, tandis que ceux qui sont répertoriés dans la clé **CompatibleHostProviders** restent en mode compatible.

 

Les paramètres suivants sont possibles :

<dl> <dt>

<span id="0"></span>0
</dt> <dd>

Spécifie que les fournisseurs s’exécutent en mode compatible.

</dd> <dt>

<span id="1"></span>1
</dt> <dd>

Spécifie que les fournisseurs s’exécutent en mode sécurisé.

</dd> </dl> </dd> </dl>

La liste suivante répertorie les paramètres de Registre possibles et les modes d’exécution associés pour un fournisseur.



| Listé sous SecuredHostProviders | Listé sous CompatibleHostProviders | Paramètre DefaultSecuredHost | Mode       |
|-----------------------------------|--------------------------------------|----------------------------|------------|
| Non                                | Non                                   | 0                          | Compatible |
| Non                                | Oui                                  | 0                          | Compatible |
| Oui                               | Non                                   | 0                          | Sécuriser     |
| Oui                               | Oui                                  | 0                          | Sécuriser     |
| Non                                | Non                                   | 1                          | Sécuriser     |
| Non                                | Oui                                  | 1                          | Compatible |
| Oui                               | Non                                   | 1                          | Sécuriser     |
| Oui                               | Oui                                  | 1                          | Sécuriser     |



 

## <a name="configuring-a-provider-to-run-in-secure-or-compatible-mode"></a>Configuration d’un fournisseur pour qu’il s’exécute en mode sécurisé ou compatible

Les clés de Registre peuvent être modifiées à l’aide de la Console de gestion des stratégies de groupe (GPMC). Pour plus d’informations, consultez [console de gestion des stratégies de groupe](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal).

Les procédures suivantes montrent comment gérer les paramètres de mode sécurisé et compatible à l’aide des préférences de stratégie de groupe. Pour plus d’informations sur les préférences de stratégie de groupe, consultez la [stratégie de groupe vue d’ensemble des préférences](/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/dn581922(v=ws.11)).

**Pour ajouter un fournisseur au mode sécurisé ou compatible à l’aide de stratégie de groupe**

1.  Ouvrez la console GPMC.
2.  Créez un objet stratégie de groupe (GPO).
3.  Modifiez l’objet de stratégie de groupe.
4.  accédez à preferences/Windows Paramètres/Registry.
5.  Cliquez avec le bouton droit et sélectionnez **nouveau... Registre**. Cette action présente une interface utilisateur dans laquelle vous pouvez entrer des informations de registre.
6.  Sélectionnez la commande **créer** .
7.  Sélectionnez le chemin d’accès à la clé de Registre suivante :

    **Mode sécurisé : HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **SecuredHostProviders**

    **Mode compatible : HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **CompatibleHostProviders**

8.  Dans le champ **nom** , entrez le nom du fournisseur que vous souhaitez ajouter à cette clé. Le nom du fournisseur doit être au format suivant : &lt; espace de noms &gt; : <\_ \_ RelPath>. Par exemple, \\ cimv2 racine : \_ \_ win32provider. Name = "MyProvider".
9.  Dans le champ **données** , entrez 0.
10. Cliquez sur OK.

**Pour supprimer un fournisseur du mode sécurisé ou compatible à l’aide de stratégie de groupe**

1.  Ouvrez la console GPMC.
2.  Créez un objet de stratégie de groupe.
3.  Modifiez l’objet de stratégie de groupe.
4.  accédez à preferences/Windows Paramètres/Registry.
5.  Cliquez avec le bouton droit et sélectionnez **nouveau... Registre**. Cette action présente une interface utilisateur dans laquelle vous pouvez entrer des informations de registre.
6.  Sélectionnez la commande **supprimer** .
7.  Sélectionnez le chemin d’accès à la clé de Registre suivante :

    **Mode sécurisé : HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **SecuredHostProviders**

    **Mode compatible : HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **CompatibleHostProviders**

8.  Dans le champ **nom** , entrez le nom du fournisseur que vous souhaitez supprimer de cette clé.
9.  Dans le champ **données** , entrez 0.
10. Cliquez sur OK.

La procédure suivante fournit des détails sur la modification du comportement des fournisseurs qui ne sont pas répertoriés dans les clés **SecuredHostProviders** ou **CompatibleHostProviders** .

**Pour modifier la valeur par défaut de la clé DefaultSecuredHost à l’aide de stratégie de groupe**

1.  Ouvrez la console GPMC.
2.  Créez un objet de stratégie de groupe.
3.  Modifiez l’objet de stratégie de groupe.
4.  accédez à preferences/Windows Paramètres/Registry.
5.  Cliquez avec le bouton droit et sélectionnez **nouveau... Registre**. Cette action présente une interface utilisateur dans laquelle vous pouvez entrer des informations de registre.
6.  Sélectionnez la commande **mettre à jour** .
7.  Sélectionnez le chemin d’accès de clé de Registre suivant : **HKEY \_ local \_ machine** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM**.
8.  Dans le champ **nom** , entrez **DefaultSecuredHost**.
9.  Dans le champ de **données** , entrez 0 pour le mode compatible ou 1 pour le mode sécurisé.
10. Cliquez sur OK.

 

 
