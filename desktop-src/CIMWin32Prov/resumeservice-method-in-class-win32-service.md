---
description: Tente de placer le service référencé dans l’État repris.
ms.assetid: 3b4228bf-9ff5-44ab-bfe2-f7dd8fb62007
ms.tgt_platform: multiple
title: Méthode ResumeService de la classe Win32_Service (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.ResumeService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ed4141b02d6e08bd4b106d2c1f72ce3fe0620fc7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861670"
---
# <a name="resumeservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a>Méthode ResumeService de la classe Win32_Service (fournisseurs WMI CIMWin32)

La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ResumeService** tente de placer le service référencé dans l’État repris.

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 ResumeService();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs répertoriées dans la liste suivante, ou toute autre valeur pour indiquer une erreur. Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**0**
</dt> <dd>

La demande a été acceptée.

</dd> <dt>

**1**
</dt> <dd>

La demande n'est pas prise en charge.

</dd> <dt>

**2**
</dt> <dd>

L’utilisateur n’a pas l’accès nécessaire.

</dd> <dt>

**3**
</dt> <dd>

Le service ne peut pas être arrêté car d'autres services en cours d'exécution en dépendent.

</dd> <dt>

**4**
</dt> <dd>

Le code de contrôle demandé n'est pas valide ou est inacceptable pour le service.

</dd> <dt>

**5**
</dt> <dd>

Le code de contrôle demandé ne peut pas être envoyé au service car l’état du service ([**Win32 \_ BaseService**](win32-baseservice.md).**** La propriété State) est égale à 0, 1 ou 2.

</dd> <dt>

**6**
</dt> <dd>

Le service n'a pas été démarré.

</dd> <dt>

**7**
</dt> <dd>

Le service n'a pas répondu à la demande de démarrage en temps voulu.

</dd> <dt>

**8**
</dt> <dd>

Échec inconnu lors du démarrage du service.

</dd> <dt>

**9**
</dt> <dd>

Le chemin d’accès au répertoire du fichier exécutable du service est introuvable.

</dd> <dt>

**10**
</dt> <dd>

Le service est déjà en cours d'exécution.

</dd> <dt>

**11**
</dt> <dd>

La base de données pour ajouter un nouveau service est verrouillée.

</dd> <dt>

**12**
</dt> <dd>

Une dépendance sur laquelle repose ce service a été supprimée du système.

</dd> <dt>

**13**
</dt> <dd>

Le service n'a pas pu trouver le service nécessaire à partir d'un service dépendant.

</dd> <dt>

**14**
</dt> <dd>

Le service a été désactivé du système.

</dd> <dt>

**15**
</dt> <dd>

Le service ne dispose pas de l'authentification correcte pour être exécuté sur le système.

</dd> <dt>

**16**
</dt> <dd>

Ce service est en cours de suppression du système.

</dd> <dt>

**17**
</dt> <dd>

Le service n’a pas de thread d’exécution.

</dd> <dt>

**19**
</dt> <dd>

Le service a des dépendances circulaires lorsqu’il démarre.

</dd> <dt>

**19**
</dt> <dd>

Un service est en cours d’exécution sous le même nom.

</dd> <dt>

**20**
</dt> <dd>

Le nom du service contient des caractères non valides.

</dd> <dt>

**21**
</dt> <dd>

Des paramètres non valides ont été transmis au service.

</dd> <dt>

**22**
</dt> <dd>

Le compte sous lequel ce service s’exécute n’est pas valide ou ne dispose pas des autorisations nécessaires pour exécuter le service.

</dd> <dt>

**23**
</dt> <dd>

Le service existe dans la base de données des services disponibles dans le système.

</dd> <dt>

**24**
</dt> <dd>

Le service est actuellement mis en pause dans le système.

</dd> </dl>

## <a name="remarks"></a>Notes

Bien qu’il puisse sembler qu’il n’y ait aucune différence pratique entre un service arrêté et un service suspendu, les deux États apparaissent différemment pour le SCM. Un service arrêté est un service qui n’est pas en cours d’exécution et doit suivre l’intégralité de la procédure de démarrage du service. Toutefois, un service suspendu est toujours en cours d’exécution, mais son fonctionnement est suspendu. Pour cette raison, un service suspendu n’a pas besoin de traverser l’intégralité de la procédure de démarrage du service, mais il a besoin d’une procédure différente pour reprendre son fonctionnement.

Vous devez utiliser la méthode appropriée pour démarrer un service qui a été arrêté ou pour reprendre un service qui a été suspendu. Les méthodes de [**\_ service Win32**](win32-service.md) [**StartService**](startservice-method-in-class-win32-service.md) et **ResumeService** doivent être utilisées dans les cas suivants :

-   Si un service est actuellement arrêté, vous devez utiliser la méthode [**StartService**](startservice-method-in-class-win32-service.md) pour le redémarrer ; **ResumeService** ne peut pas démarrer un service qui est actuellement arrêté.
-   Si un service est suspendu, vous devez utiliser **ResumeService**. Si vous utilisez la méthode [**StartService**](startservice-method-in-class-win32-service.md) sur un service suspendu, vous recevez le message « le service est déjà en cours d’exécution ». Toutefois, le service reste en pause jusqu’à ce que le code de contrôle de reprise du service lui soit envoyé.

## <a name="examples"></a>Exemples

L’exemple de [reprise des services AutoStart qui sont en pause](https://Gallery.TechNet.Microsoft.Com/413f2896-e7f3-4b3e-96cb-5abdc9bb6c36) VBScript redémarre tous les services à démarrage automatique qui ont été suspendus.

L’exemple de code VBScript suivant décrit comment reprendre un service suspendu à partir d’instances [**du \_ service Win32**](win32-service.md).

> [!Note]  
> Le service doit prendre en charge la suspension et être déjà en cours d’exécution.

 


```VB
Set ServiceSet = GetObject("winmgmts:").ExecQuery("select * from Win32_Service where Name='Schedule'")

for each Service in ServiceSet
 SupportsPause = Service.AcceptPause
 if SupportsPause = true then
  RetVal = Service.ResumeService()
  if RetVal = 0 then 
   WScript.Echo "Service resumed"   
  else
   if RetVal = 1 then 
    WScript.Echo "Pause not supported" 
   else WScript.Echo "An error occurred:" & RetVal
   End If
  End If
 else
  WScript.Echo "Service does not support pause"
 end if
next
```



L’exemple de code perl suivant décrit comment reprendre un service suspendu à partir d’instances [**du \_ service Win32**](win32-service.md).

> [!Note]  
> Le service doit prendre en charge la suspension et être déjà en cours d’exécution.

 


```Perl
use strict;
use Win32::OLE;

my $ServiceSet;

eval { $ServiceSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\Root\\CIMv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='Schedule'"); };

if (!$@ && defined $ServiceSet)
{
 foreach my $Service (in $ServiceSet)
 {
  my $SupportsPause = $Service->{AcceptPause};
  if ($SupportsPause)
  {
   my $RetVal = $Service->ResumeService();
   if ($RetVal == 0)
   {
    print "\nService resumed\n";
   }
   else
   {
    if ($RetVal == 1)
    {
     print STDERR "\nPause not supported\n";
    }
    else
    {
     print STDERR "\nAn error occurred: ", $RetVal, "\n";
    }
   }
  }
  else
  {
   print "\nService does not support pause\n";
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | Racine\\CIMv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Service Win32**](win32-service.md)
</dt> <dt>

[Tâches WMI : services](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

