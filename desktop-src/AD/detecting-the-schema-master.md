---
title: Détection du contrôleur de schéma
description: Active Directory Domain Services disposez d’un système de mise à jour multimaître ; chaque contrôleur de domaine contient une copie accessible en écriture de l’annuaire.
ms.assetid: 8e096351-43f8-48ee-acb6-681d9e38e93c
ms.tgt_platform: multiple
keywords:
- Détection de l’AD du contrôleur de schéma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6869853cba68d7155f2091e2fe4515116944a629
ms.sourcegitcommit: f730b85cc85448913e50a7f331e10b646ea7978b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/23/2019
ms.locfileid: "103840934"
---
# <a name="detecting-the-schema-master"></a>Détection du contrôleur de schéma

Active Directory Domain Services disposez d’un système de mise à jour multimaître ; chaque contrôleur de domaine contient une copie accessible en écriture de l’annuaire. Les mises à jour de schéma sont propagées à tous les domaines qui appartiennent à la même arborescence ou forêt. Étant donné qu’il est difficile de rapprocher les mises à jour conflictuelles du schéma, les mises à jour de schéma ne peuvent être effectuées que sur un seul serveur. Le serveur ayant le droit d’effectuer des mises à jour peut changer, mais un seul serveur aura ce droit à un moment donné. Ce serveur est appelé le contrôleur de schéma. Le premier contrôleur de bus installé dans une entreprise est, par défaut, le contrôleur de schéma.

Les modifications de schéma ne peuvent être effectuées qu’au niveau du contrôleur de schéma. Pour détecter le contrôleur de bus de schéma, procédez comme suit.

**Détection du contrôleur de schéma DC**

1.  Lisez l’attribut **fSMORoleOwner** du conteneur de schéma sur n’importe quel contrôleur de périphérique. L’attribut **fSMORoleOwner** retourne le nom unique (DN) de l’objet **nTDSDSA** pour le contrôleur de schéma.
2.  Liez l’objet **nTDSDSA** dont vous venez de récupérer le nom unique. Le parent de cet objet est l’objet serveur pour le contrôleur de bus contenant le contrôleur de schéma.
3.  Obtient l’ADsPath du parent de l’objet **nTDSDSA** . Le parent est un objet serveur.
4.  Lier à l’objet serveur.
5.  Obtient l’attribut **dNSHostName** de l’objet serveur. Il s’agit du nom DNS du contrôleur de domaine qui contient le contrôleur de schéma.
6.  Spécifiez le nom DNS du contrôleur de schéma en tant que serveur et DN comme nom unique du conteneur de schéma à lier au contrôleur de schéma. Par exemple, si le serveur était « dc1.fabrikam.com » et que le nom de domaine du conteneur de schéma était « CN = Schema, CN = Configuration, DC = fabrikam, DC = com », le chemin ADsPath serait le suivant.
    ```C++
    LDAP://dc1.fabrikam.com/cn=schema,cn=configuration,dc=fabrikam,dc=com
    ```

    

Il est recommandé de trouver le contrôleur de schéma et de vous y lier pour apporter des modifications au schéma. Toutefois, vous pouvez déplacer le contrôleur de schéma vers un autre serveur.

Pour faire d’un autre serveur le contrôleur de schéma, un utilisateur convenablement privilégié peut effectuer les opérations suivantes :

-   Utilisez le composant logiciel enfichable MMC du gestionnaire de schémas.
    > [!Note]
    > Le composant logiciel enfichable MMC du schéma Active Directory doit être inscrit manuellement. Pour inscrire le composant logiciel enfichable Schéma, vous devez exécuter la commande suivante à partir de l’invite de commandes dans le répertoire system32 de Windows.
    >
    > **regsvr32.exe schmmgmt.dll**

     

-   Utilisez l’utilitaire de ligne de commande NTDSUTIL.
-   Utilisez une application tierce (une application qui émet l’écriture LDAP appropriée).

Pour devenir le contrôleur de schéma par programme, une application exécutée dans le contexte d’un utilisateur convenablement privilégié peut émettre une écriture LDAP de l’attribut opérationnel **becomeSchemaMaster** vers le RootDSE sur ce contrôleur de périphérique. Cela lance un transfert atomique du contrôleur de schéma directement à partir du détenteur actuel vers le contrôleur de bus local.

L’exemple de code suivant recherche le contrôleur de schéma. La fonction suivante est liée au conteneur de schéma sur l’ordinateur qui est le contrôleur de schéma.


```C++
HRESULT BindToSchemaMaster(IADsContainer **ppSchemaMaster)
{
HRESULT hr = E_FAIL;
// Get rootDSE and the schema container DN.
IADs *pObject = NULL;
IADs *pTempSchema = NULL;
IADs *pNTDS = NULL;
IADs *pServer = NULL;
BSTR bstrParent;
LPOLESTR szPath = new OLECHAR[MAX_PATH];
VARIANT var, varRole,varComputer;
hr = ADsOpenObject(L"LDAP://rootDSE",
         NULL,
         NULL,
         ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
         IID_IADs,
         (void**)&pObject);
if (hr == S_OK)
{
  hr = pObject->Get(CComBSTR("schemaNamingContext"), &var);
  if (hr == S_OK)
  {
    wcscpy_s(szPath,L"LDAP://");
    wcscat_s(szPath,var.bstrVal);
    hr = ADsOpenObject(szPath,
             NULL,
             NULL,
             ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
             IID_IADs,
             (void**)&pTempSchema);
 
    if (hr == S_OK)
    {
      /*
      Read the fsmoRoleOwner attribute to identify which server is 
      the schema master.
      */  
      hr = pTempSchema->Get(CComBSTR("fsmoRoleOwner"), &varRole);
      if (hr == S_OK)
      {
        // The fsmoRoleOwner attribute returns the nTDSDSA object.
        // The parent is the server object.
        // Bind to NTDSDSA object and get parent.
        wcscpy_s(szPath,L"LDAP://");
        wcscat_s(szPath,varRole.bstrVal);
        hr = ADsOpenObject(szPath,
             NULL,
             NULL,
             ADS_SECURE_AUTHENTICATION,
             IID_IADs,
             (void**)&pNTDS);
        if (hr == S_OK)
        {
          hr = pNTDS->get_Parent(&bstrParent);
          if (hr == S_OK)
          {
            /*
            Bind to server object and get the DNS name of 
            the server.
            */
            wcscpy_s(szPath,bstrParent);
            hr = ADsOpenObject(szPath,
               NULL,
               NULL,
               ADS_SECURE_AUTHENTICATION,
               IID_IADs,
               (void**)&pServer);
            if (hr == S_OK)
            {
              // Get the dns name of the server.
              hr = pServer->Get(CComBSTR("dNSHostName"), 
                  &varComputer);
              if (hr == S_OK)
              {
                    wcscpy_s(szPath,L"LDAP://");
                    wcscat_s(szPath,varComputer.bstrVal);
                    wcscat_s(szPath,L"/");
                    wcscat_s(szPath,var.bstrVal);
                    hr = ADsOpenObject(szPath,
                         NULL,
                         NULL,
                         ADS_SECURE_AUTHENTICATION,
                         IID_IADs,
                         (void**)ppSchemaMaster);
                    if (FAILED(hr))
                    {
                      if (*ppSchemaMaster)
                      {
                        (*ppSchemaMaster)->Release();
                        (*ppSchemaMaster) = NULL;
                      }
                    }
              }
              VariantClear(&varComputer);
            }
            if (pServer)
              pServer->Release();
          }
          SysFreeString(bstrParent);
        }
        if (pNTDS)
          pNTDS->Release();
      }
      VariantClear(&varRole);
    }
    if (pTempSchema)
      pTempSchema->Release();
  }
  VariantClear(&var);
}
if (pObject)
    pObject->Release();
 
return hr;
}
```



L’exemple de code suivant affiche le nom DNS de l’ordinateur qui est le contrôleur de schéma.


```VB
On Error Resume Next
 
'''''''''''''''''''
' Bind to the rootDSE
''''''''''''''''''''
sPrefix = "LDAP://"
Set root= GetObject(sPrefix & "rootDSE")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method"
End If
 
'''''''''''''''''''
' Get the DN for the schema
''''''''''''''''''''
sSchema = root.Get("schemaNamingContext")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on Get method"
End If
 
'''''''''''''''''''
' Bind to the schema container
''''''''''''''''''''
Set Schema= GetObject(sPrefix & sSchema )
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method to bind to schema"
End If
''''''''''''''''''''
' Read the fsmoRoleOwner attribute to see which server is the 
' schema master.
''''''''''''''''''''
sMaster = Schema.Get("fsmoRoleOwner")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::Get method for fsmoRoleOwner"
End If
''''''''''''''''''''
' The fsmoRoleOwner attribute returns the nTDSDSA object.
' The parent is the server object.
' Bind to NTDSDSA object and get the parent object.
''''''''''''''''''''
Set NTDS = GetObject(sPrefix & sMaster)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for NTDS"
End If
sServer = NTDS.Parent
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::get_Parent method"
End If
''''''''''''''''''''
' Bind to server object
' and get the reference to the computer object.
''''''''''''''''''''
Set Server = GetObject(sServer)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for " & sServer
End If
sComputer = Server.Get("dNSHostName")
''''''''''''''''''''
' Display the DNS name for the computer.
''''''''''''''''''''
strText = "Schema master has the following DNS name: "& sComputer
WScript.echo strText
 
 
 
''''''''''''''''''''
' Display subroutines
''''''''''''''''''''
 
Sub BailOnFailure(ErrNum, ErrText)
    strText = "Error 0x" & Hex(ErrNum) & " " & ErrText
    MsgBox strText, vbInformation, "ADSI Error"
    WScript.Quit
End Sub
```



 

 




