---
title: Moniker d’élévation COM
description: Le moniker d’élévation COM autorise les applications qui s’exécutent sous le contrôle de compte d’utilisateur (UAC) à activer des classes COM avec des privilèges élevés. Pour plus d’informations, consultez focus sur le moindre privilège.
ms.assetid: 1595ebb8-65af-4609-b3e7-a21209e64391
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc80774764cb99e63ed3334a8c0f9c8cedd2500
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363624"
---
# <a name="the-com-elevation-moniker"></a>Moniker d’élévation COM

Le moniker d’élévation COM autorise les applications qui s’exécutent sous le contrôle de compte d’utilisateur (UAC) à activer des classes COM avec des privilèges élevés. Pour plus d’informations, consultez [focus sur le moindre privilège](/previous-versions/dotnet/articles/aa480194(v=msdn.10)).

## <a name="when-to-use-the-elevation-moniker"></a>Quand utiliser le moniker d’élévation

Le moniker d’élévation est utilisé pour activer une classe COM afin d’accomplir une fonction spécifique et limitée qui requiert des privilèges élevés, tels que la modification de la date et de l’heure système.

L’élévation nécessite la participation à la fois d’une classe COM et de son client. La classe COM doit être configurée pour prendre en charge l’élévation en annotant son entrée de Registre, comme décrit dans la section Configuration requise. Le client COM doit demander une élévation à l’aide du moniker d’élévation.

Le moniker d’élévation n’est pas destiné à fournir la compatibilité des applications. Par exemple, si vous souhaitez exécuter une application COM héritée telle que WinWord comme un serveur avec élévation de privilèges, vous devez configurer l’exécutable du client COM pour exiger une élévation, plutôt que d’activer la classe de l’application héritée avec le moniker d’élévation. Lorsque le client COM avec élévation de privilèges appelle [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) à l’aide du CLSID de l’application héritée, l’état élevé du client est transmis au processus serveur.

Toutes les fonctionnalités COM ne sont pas compatibles avec l’élévation. Les fonctionnalités qui ne fonctionnent pas incluent :

-   L’élévation ne passe pas d’un client à un serveur COM distant. Si un client Active un serveur COM distant avec le moniker d’élévation, le serveur n’est pas élevé, même s’il prend en charge l’élévation.
-   Si une classe COM avec élévation de privilèges utilise l’emprunt d’identité pendant un appel COM, elle risque de perdre ses privilèges élevés pendant l’emprunt d’identité.
-   Si un serveur COM avec élévation de privilèges enregistre une classe dans la table ROT (Running Object Table), la classe ne sera pas disponible pour les clients non élevés.
-   Un processus élevé à l’aide du mécanisme de contrôle de compte d’utilisateur ne charge pas les classes par utilisateur lors des activations COM. Pour les applications COM, cela signifie que les classes COM de l’application doivent être installées dans la ruche de Registre **HKEY \_ local \_ machine** si l’application doit être utilisée à la fois par des comptes non privilégiés et privilégiés. Les classes COM de l’application doivent uniquement être installées dans la ruche des **\_ utilisateurs HKEY** si l’application n’est jamais utilisée par des comptes privilégiés.
-   La fonction glisser-déplacer n’est pas autorisée pour les applications avec élévation de privilèges non élevées.

## <a name="requirements"></a>Spécifications

Afin d’utiliser le moniker d’élévation pour activer une classe COM, la classe doit être configurée pour s’exécuter en tant qu’utilisateur de lancement ou en tant qu’identité d’application’Activate As Activator'. Si la classe est configurée pour s’exécuter sous n’importe quelle autre identité, l’activation retourne l’erreur la valeur de CO \_ E \_ runas \_ \_ doit \_ être \_ AAA.

La classe doit également être annotée avec un nom d’affichage « convivial » compatible avec l’interface utilisateur multilingue (MUI). Pour cela, vous devez disposer de l’entrée de Registre suivante :

```
HKEY_LOCAL_MACHINE\Software\Classes\CLSID
   {CLSID}
      LocalizedString = displayName
```

Si cette entrée est manquante, l’activation renvoie le message d’erreur «le \_ \_ DisplayName est manquant \_ . Si le fichier MUI est manquant, le code d’erreur de la fonction [**RegLoadMUIStringW**](/windows/desktop/api/winreg/nf-winreg-regloadmuistringa) est retourné.

Si vous le souhaitez, pour spécifier une icône d’application à afficher par l’interface utilisateur du contrôle de compte d’utilisateur, ajoutez la clé de Registre suivante :

```
HKEY_LOCAL_MACHINE\Software\Classes\CLSID
   {CLSID}
      Elevation
         IconReference = applicationIcon
```

**IconReference** utilise le même format que **LocalizedString**:

@*pathtobinary*,*-resourcenumber*

En outre, le composant COM doit être signé pour que l’icône s’affiche.

La classe COM doit également être annotée comme étant compatible LUA. Pour cela, vous devez disposer de l’entrée de Registre suivante :

```
HKEY_LOCAL_MACHINE\Software\Classes\CLSID
   {CLSID}
      Elevation
         Enabled = 1
```

Si cette entrée est manquante, l’activation retourne l’erreur CO \_ E \_ Elévation \_ désactivée.

Notez que ces entrées doivent exister dans la \_ ruche HKEY local \_ machine, et non dans la \_ ruche HKEY Current \_ User ou HKEY \_ users. Cela empêche les utilisateurs d’élever les classes COM qu’ils n’ont pas également les privilèges nécessaires pour s’inscrire.

## <a name="the-elevation-moniker-and-the-elevation-ui"></a>Moniker de l’élévation et interface utilisateur d’élévation

Si le client est déjà élevé, l’utilisation du moniker d’élévation n’entraîne pas l’affichage de l’interface utilisateur d’élévation.

## <a name="how-to-use-the-elevation-moniker"></a>Comment utiliser le moniker d’élévation

Le moniker d’élévation est un moniker COM standard, similaire aux monikers de session, de partition ou de file d’attente. Il dirige une demande d’activation vers un serveur spécifié avec le niveau d’élévation spécifié. Le CLSID à activer apparaît dans la chaîne de moniker.

Le moniker d’élévation prend en charge les jetons de niveau d’exécution suivants :

1.  Administrateur
2.  Le plus élevé

La syntaxe est la suivante :

``` syntax
Elevation:Administrator!new:{guid}
Elevation:Highest!new:{guid}
```

La syntaxe précédente utilise le moniker « New » pour retourner une instance de la classe COM spécifiée par *GUID*. Notez que le moniker « New » utilise en interne l’interface [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) pour obtenir un objet de classe, puis appelle [**IClassFactory :: CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) sur ce dernier.

Le moniker de l’élévation peut également être utilisé pour obtenir un objet de classe, qui implémente [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory). L’appelant appelle ensuite [**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) pour recevoir une instance d’objet. La syntaxe est la suivante :

``` syntax
Elevation:Administrator!clsid:{guid}
```

## <a name="sample-code"></a>Exemple de code

L’exemple de code suivant montre comment utiliser le moniker d’élévation. Il part du principe que vous avez déjà initialisé COM sur le thread actuel.


```C++
HRESULT CoCreateInstanceAsAdmin(HWND hwnd, REFCLSID rclsid, REFIID riid, __out void ** ppv)
{
    BIND_OPTS3 bo;
    WCHAR  wszCLSID[50];
    WCHAR  wszMonikerName[300];

    StringFromGUID2(rclsid, wszCLSID, sizeof(wszCLSID)/sizeof(wszCLSID[0])); 
    HRESULT hr = StringCchPrintf(wszMonikerName, sizeof(wszMonikerName)/sizeof(wszMonikerName[0]), L"Elevation:Administrator!new:%s", wszCLSID);
    if (FAILED(hr))
        return hr;
    memset(&bo, 0, sizeof(bo));
    bo.cbStruct = sizeof(bo);
    bo.hwnd = hwnd;
    bo.dwClassContext  = CLSCTX_LOCAL_SERVER;
    return CoGetObject(wszMonikerName, &bo, riid, ppv);
}
```



[**Liaison \_ OPTS3**](/windows/win32/api/objidl/ns-objidl-bind_opts3~r1) est une nouveauté de Windows Vista. Elle est dérivée de [**Bind \_ OPTS2**](/windows/win32/api/objidl/ns-objidl-bind_opts2~r1).

Le seul ajout est un champ **HWND** , **HWND**. Ce handle représente une fenêtre qui devient le propriétaire de l’interface utilisateur d’élévation, le cas échéant.

Si **HWND** a la **valeur null**, com appellera [GetActiveWindow](/windows/win32/api/winuser/nf-winuser-getactivewindow) pour trouver un handle de fenêtre associé au thread actuel. Ce cas peut se produire si le client est un script, qui ne peut pas remplir une structure [**\_ OPTS3 de liaison**](/windows/win32/api/objidl/ns-objidl-bind_opts3~r1) . Dans ce cas, COM essaiera d’utiliser la fenêtre associée au thread de script.

## <a name="over-the-shoulder-ots-elevation"></a>Élévation à l’épaule (OTS)

L’élévation de la valeur par rapport à l’épaule (OTS) fait référence au scénario dans lequel un client exécute un serveur COM avec les informations d’identification d’un administrateur plutôt que son propre. (Le terme « à l’épaule » signifie que l’administrateur regarde l’épaule du client au fur et à mesure que le client exécute le serveur.)

Ce scénario peut provoquer un problème pour les appels COM dans le serveur, car le serveur peut ne pas appeler [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) de manière explicite (autrement dit, par programmation) ou implicitement (c’est-à-dire, de manière déclarative, à l’aide du registre). Pour ces serveurs, COM calcule un descripteur de sécurité qui autorise uniquement les administrateurs SELF, SYSTEM et builtin \\ à effectuer des appels com sur le serveur. Cette configuration ne fonctionne pas dans les scénarios OTS. Au lieu de cela, le serveur doit appeler **CoInitializeSecurity**, de manière explicite ou implicite, et spécifier une liste de contrôle d’accès qui comprend le SID et le système du groupe interactif.

L’exemple de code suivant montre comment créer un descripteur de sécurité (SD) avec le SID de groupe interactif.

``` syntax
BOOL GetAccessPermissionsForLUAServer(SECURITY_DESCRIPTOR **ppSD)
{
// Local call permissions to IU, SY
    LPWSTR lpszSDDL = L"O:BAG:BAD:(A;;0x3;;;IU)(A;;0x3;;;SY)";
    SECURITY_DESCRIPTOR *pSD;
    *ppSD = NULL;

    if (ConvertStringSecurityDescriptorToSecurityDescriptorW(lpszSDDL, SDDL_REVISION_1, (PSECURITY_DESCRIPTOR *)&pSD, NULL))
    {
        *ppSD = pSD;
        return TRUE;
    }

    return FALSE;
}
```

L’exemple de code suivant montre comment appeler [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) implicitement avec le SD à partir de l’exemple de code précédent :


```C++
// hKey is the HKCR\AppID\{GUID} key
BOOL SetAccessPermissions(HKEY hkey, PSECURITY_DESCRIPTOR pSD)
{
    BOOL bResult = FALSE;
    DWORD dwLen = GetSecurityDescriptorLength(pSD);
    LONG lResult;
    lResult = RegSetValueExA(hkey, 
        "AccessPermission",
        0,
        REG_BINARY,
        (BYTE*)pSD,
        dwLen);
    if (lResult != ERROR_SUCCESS) goto done;
    bResult = TRUE;
done:
    return bResult;
}
```



L’exemple de code suivant montre comment appeler [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) explicitement avec le SD ci-dessus :


```C++
// Absolute SD values
PSECURITY_DESCRIPTOR pAbsSD = NULL;
DWORD AbsSdSize = 0;
PACL  pAbsAcl = NULL;
DWORD AbsAclSize = 0;
PACL  pAbsSacl = NULL;
DWORD AbsSaclSize = 0;
PSID  pAbsOwner = NULL;
DWORD AbsOwnerSize = 0;
PSID  pAbsGroup = NULL;
DWORD AbsGroupSize = 0;

MakeAbsoluteSD (
    pSD,
    pAbsSD,
    &AbsSdSize,
    pAbsAcl,
    &AbsAclSize,
    pAbsSacl,
    &AbsSaclSize,
    pAbsOwner,
    &AbsOwnerSize,
    pAbsGroup,
    &AbsGroupSize
);

if (ERROR_INSUFFICIENT_BUFFER == GetLastError())
{
    pAbsSD = (PSECURITY_DESCRIPTOR)LocalAlloc(LMEM_FIXED, AbsSdSize);
    pAbsAcl = (PACL)LocalAlloc(LMEM_FIXED, AbsAclSize);
    pAbsSacl = (PACL)LocalAlloc(LMEM_FIXED, AbsSaclSize);
    pAbsOwner = (PSID)LocalAlloc(LMEM_FIXED, AbsOwnerSize);
    pAbsGroup = (PSID)LocalAlloc(LMEM_FIXED, AbsGroupSize);

    if ( ! (pAbsSD && pAbsAcl && pAbsSacl && pAbsOwner && pAbsGroup))
    {
        hr = E_OUTOFMEMORY;
        goto Cleanup;
    }
    if ( ! MakeAbsoluteSD(
        pSD,
        pAbsSD,
        &AbsSdSize,
        pAbsAcl,
        &AbsAclSize,
        pAbsSacl,
        &AbsSaclSize,
        pAbsOwner,
        &AbsOwnerSize,
        pAbsGroup,
        &AbsGroupSize
        ))
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        goto Cleanup;
    }
}
else
{
    hr = HRESULT_FROM_WIN32(GetLastError());
    goto Cleanup;
}

// Call CoinitilizeSecurity.
```



## <a name="com-permissions-and-mandatory-access-labels"></a>Autorisations COM et étiquettes d’accès obligatoires

Windows Vista introduit la notion d' *étiquettes d’accès obligatoires* dans les descripteurs de sécurité. L’étiquette détermine si les clients peuvent obtenir un accès en exécution à un objet COM. L’étiquette est spécifiée dans la partie liste de contrôle d’accès système (SACL) du descripteur de sécurité. dans Windows Vista, COM prend en charge l’étiquette \_ \_ non exécuter le nom obligatoire du système \_ \_ \_ . les listes sacl dans les autorisations COM sont ignorées sur les systèmes d’exploitation antérieurs à Windows Vista.

à partir de Windows Vista, dcomcnfg.exe ne prend pas en charge la modification du niveau d’intégrité (IL) dans les autorisations COM. Elle doit être définie par programmation.

L’exemple de code suivant montre comment créer un descripteur de sécurité COM avec une étiquette qui autorise les demandes de lancement/activation à partir de tous les clients IL bas. Notez que les étiquettes sont valides pour les autorisations de lancement/activation et d’appel. Par conséquent, il est possible d’écrire un serveur COM qui interdit le lancement, l’activation ou les appels des clients avec un langage intermédiaire donné. pour plus d’informations sur les niveaux d’intégrité, consultez la section « fonctionnement du mécanisme d’intégrité de Windows Vista » dans [présentation et utilisation du Mode protégé d’Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/).


```C++
BOOL GetLaunchActPermissionsWithIL (SECURITY_DESCRIPTOR **ppSD)
{
// Allow World Local Launch/Activation permissions. Label the SD for LOW IL Execute UP
    LPWSTR lpszSDDL = L"O:BAG:BAD:(A;;0xb;;;WD)S:(ML;;NX;;;LW)";
    if (ConvertStringSecurityDescriptorToSecurityDescriptorW(lpszSDDL, SDDL_REVISION_1, (PSECURITY_DESCRIPTOR *)&pSD, NULL))
    {
        *ppSD = pSD;
        return TRUE;
    }
}

BOOL SetLaunchActPermissions(HKEY hkey, PSECURITY_DESCRIPTOR pSD)
{
    
    BOOL bResult = FALSE;
    DWORD dwLen = GetSecurityDescriptorLength(pSD);
    LONG lResult;
    lResult = RegSetValueExA(hkey, 
        "LaunchPermission",
        0,
        REG_BINARY,
        (BYTE*)pSD,
        dwLen);
    if (lResult != ERROR_SUCCESS) goto done;
    bResult = TRUE;
done:
    return bResult;
};
```



## <a name="cocreateinstance-and-integrity-levels"></a>CoCreateInstance et niveaux d’intégrité

le comportement de [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) a changé dans Windows Vista, afin d’empêcher les clients IL bas de se lier aux serveurs COM par défaut. Le serveur doit autoriser explicitement ces liaisons en spécifiant la liste SACL. Les modifications apportées à **CoCreateInstance** sont les suivantes :

1.  Lors du lancement d’un processus serveur COM, le langage intermédiaire du jeton de processus serveur est défini sur le langage intermédiaire du client ou du serveur, selon la valeur la plus basse.
2.  Par défaut, COM empêche les clients IL bas de se lier aux instances en cours d’exécution de tous les serveurs COM. Pour autoriser la liaison, le descripteur de sécurité de lancement/activation d’un serveur COM doit contenir une liste SACL qui spécifie l’étiquette IL faible (consultez la section précédente pour l’exemple de code pour créer un tel descripteur de sécurité).

## <a name="elevated-servers-and-rot-registrations"></a>Serveurs élevés et inscriptions ROT

Si un serveur COM souhaite s’inscrire dans la table ROT (Running Object Table) et autoriser n’importe quel client à accéder à l’inscription, il doit utiliser l' \_ indicateur ROTFLAGS ALLOWANYCLIENT. Un serveur COM « Activate As Activator » ne peut pas spécifier ROTFLAGS \_ ALLOWANYCLIENT, car le gestionnaire de contrôle des services DCOM (DCOMSCM) applique un contrôle d’usurpation d’identité à cet indicateur. par conséquent, dans Windows Vista, COM ajoute la prise en charge d’une nouvelle entrée de registre qui permet au serveur de stipuler que ses inscriptions ROT sont mises à la disposition de n’importe quel client :

```
HKEY_LOCAL_MACHINE\Software\Classes\AppID
   {APPID}
      ROTFlags
```

La seule valeur valide pour cette entrée de Registre \_ DWORD est :

``` syntax
ROTREGFLAGS_ALLOWANYCLIENT 0x1
```

L’entrée doit exister dans la ruche **HKEY \_ local \_ machine** .

Cette entrée fournit un serveur « Activate As Activator » avec les mêmes fonctionnalités que celles fournies par ROTFLAGS \_ ALLOWANYCLIENT pour un serveur runas.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Sécurité dans COM](security-in-com.md)
</dt> <dt>

[Présentation et utilisation d’Internet Explorer en mode protégé](/previous-versions/windows/internet-explorer/ie-developer/)
</dt> </dl>

 

 