---
description: la \_ classe Win32 ServerFeature représente les fonctionnalités installées sur un ordinateur exécutant Windows Server.
ms.assetid: fe3bb95c-7f69-47b5-9c3d-771cdc3ed9ca
ms.tgt_platform: multiple
title: Win32_ServerFeature, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ServerFeature
- Win32_ServerFeature.ID
- Win32_ServerFeature.ParentID
- Win32_ServerFeature.Name
api_type:
- DllExport
api_location:
- ServerCompProv.dll
ms.openlocfilehash: eddbd71108a5b6b65de329e1c110c965f437e4c24f7ba0a681935ba5075351fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312136"
---
# <a name="win32_serverfeature-class"></a>\_Classe ServerFeature Win32

\[La classe **Win32 \_ ServerFeature** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. Au lieu de cela, utilisez les [classes du fournisseur ServerManager deploymentProvider](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment).\]

la classe **Win32 \_ ServerFeature** représente les fonctionnalités installées sur un ordinateur exécutant Windows Server.

Cette classe peut être utilisée par les développeurs et les administrateurs qui doivent automatiser le processus de détermination des fonctionnalités installées sur un ensemble d’ordinateurs serveurs. Les instances de cette classe ne sont pas disponibles sur les ordinateurs clients.

## <a name="syntax"></a>Syntaxe

``` syntax
[Deprecated("No value"), Dynamic, Provider("ServerFeatureProvider"), AMENDMENT]
class Win32_ServerFeature
{
  uint32 ID;
  uint32 ParentID;
  string Name;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ ServerFeature** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ ServerFeature** a ces propriétés.

<dl> <dt>

**Identifiant**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**clé**](key-qualifier.md), [**non \_ null**](optional-qualifiers.md)
</dt> </dl>

ID de la fonctionnalité serveur. La liste suivante répertorie les valeurs possibles de la propriété ID :



Valeur

Nom

1

[Serveur d’applications](/windows)

2

Serveur Web (IIS)

3

[Services de diffusion multimédia en continu](/windows)

5

Serveur de télécopie

6

Services de fichiers et iSCSI<br/> [changement de nom](/windows)<br/>

7

Services d'impression et de numérisation de document<br/> [changement de nom](/windows)<br/>

8

[Active Directory Federation Services](/windows)

9

Services AD LDS (Active Directory Lightweight Directory Services)

10

Active Directory Domain Services

11

[Services UDDI](/windows)<br/>

12

[Serveur DHCP](/windows)

13

[Serveur DNS](/windows)

14

Network Policy and Access Services

16

Services de certificats Active Directory

17

Services AD RMS (Active Directory Rights Management Services)

18

[Services Bureau à distance](/windows)<br/> [changement de nom](/windows)<br/>

19

Services de déploiement Windows

20

Hyper-V

21

[Windows Server Update Services](/windows)

33

[Clustering de basculement](/windows)

34

[Équilibrage de la charge réseau](/windows)

36

[Fonctionnalités .NET Framework 3.5.1](/windows)<br/> [changement de nom](/windows)<br/>

37

[Gestionnaire de ressources système Windows](/windows)

38

Service de réseau local sans fil

39

[Windows Fonctionnalités de sauvegarde du serveur](/windows)

40

Serveur WINS

41

Service d’activation des processus Windows

42

[Assistance à distance](/windows)

43

Services TCP/IP simples

44

[Client Telnet](/windows)

45

[Serveur Telnet](/windows)

46

[Sous-système pour les applications UNIX](/windows)

47

Proxy RPC sur HTTP

48

SMTP Server (Serveur SMTP)

49

Message Queuing

51

[Base de données interne Windows](/windows)

52

[Stockage Gestionnaire pour réseau San](/windows)

53

Moniteur de port LPR

55

[Serveur de nom de stockage Internet](/windows)

57

[MPIO (Multipath I/O)](/windows)

58

Client TFTP

59

[Services SNMP](/windows)

60

[gestionnaire de Stockage amovible](/windows)

61

Chiffrement de lecteur BitLocker

62

[Services pour le système de fichiers réseau](/windows)

63

Client d'impression Internet

64

[Protocole PNRP (Peer Name Resolution Protocol)](/windows)

65

Kit d'administration du Gestionnaire des connexions Microsoft

66

[Windows PowerShell](/windows)<br/>

67

[Outils d'administration de serveur distant](/windows)

68

[Expérience audio-vidéo haute qualité Windows](/windows)

69

[Gestion des stratégies de groupe](/windows)

71

[service d'indexation](/windows)

72

[Gestionnaire de ressources du serveur de fichiers](/windows)

73

Compression différentielle à distance

310

Services de prise en charge de l'écriture manuscrite<br/>

320

[Outils de migration de Windows Server](/windows)<br/>

321

[Extension WinRM IIS](/windows)<br/>

324

[BranchCache](#branchcache)<br/>

334

[Console de gestion DirectAccess](/windows)<br/>

335

[Service de transfert intelligent en arrière-plan (BITS)](/windows)<br/>

338

[Visionneuse XPS](/windows)<br/>

339

[Windows Biometric Framework](/windows)<br/>

340

Prise en charge WoW64<br/>

351

[Windows PowerShell Environnement d’écriture de scripts intégré (ISE)](/windows)<br/>

352

Windows TIFF IFilter<br/>

404

[Services de mise à jour Windows Server](/windows)

409

[Serveur de gestion des adresses IP (IPAM)](/windows)

417

[Windows PowerShell](/windows)

418

[.NET Framework 4.5](/windows)

432

[Service Windows Search](/windows)

438

[Client pour NFS](/windows)

441

[Déverrouillage réseau BitLocker](/windows)

442

[Extension ISS Management OData](/windows)

450

[.NET Framework 4.5 Advanced Services](/windows)

466

[Fonctionnalités de .NET Framework 4.5](/windows)

468

[Accès à distance](/windows)<br/>

477

[Interfaces utilisateur et infrastructure](/windows)

478

[Outils de gestion graphiques et infrastructure](/windows)

481

[Services de fichiers et de stockage](/windows)

485

[Expérience Windows Server Essentials](/windows)

488

[DirectPlay](/windows)

Services de fichiers-services de rôle (6)

Valeur

Nom

100

[système de fichiers DFS](/windows)

101

Espace de noms DFS

102

Réplication DFS

103

[Service de réplication de fichiers](/windows)

104

[Gestionnaire de ressources du serveur de fichiers](/windows)

105

[Services pour le système de fichiers réseau](/windows)

106

[Stockage d’instance simple](/windows)

107

[Service Windows Search](/windows)

108

[service d'indexation](/windows)

255

Serveur de fichiers

350

BranchCache pour fichiers réseau

431

[Serveur pour NFS](/windows)<br/>

434

[Service Agent VSS du serveur de fichiers](/windows)<br/>

435

[Serveur cible iSCSI](/windows)<br/>

436

[Déduplication des données](/windows)<br/>

437

[fournisseur de Stockage de la cible iSCSI (fournisseurs de matériel VDS et VSS)](/windows)

486

[Dossiers de travail](/windows)

Services de rôle AD DS (10)

Valeur

Nom

110

[Contrôleur de domaine Active Directory](/windows)

111

[Gestion des identités pour UNIX](/windows)

112

[Serveur pour Network Information Services](/windows)

113

[Synchronisation de mot de passe](/windows)

294

[Outils d'administration de serveur distant](/windows)

Diffusion multimédia-services de rôle (3)

Valeur

Nom

120

[Windows Serveur multimédia](/windows)

121

[Administration basée sur le Web](/windows)

122

[Agent de journalisation](/windows)

ADFS-services de rôle (8)

Valeur

Nom

125

[Active Directory Federation Services](/windows)

126

[Stratégie de service FS (Federation Service)](/windows)

127

[Agents Web AD FS](/windows)

128

[Agent prenant en charge les revendications](/windows)

129

[Windows Agent basé sur les jetons](/windows)

Services de rôle Services Bureau à distance (18)

Valeur

Nom

130

Hôte de session Bureau à distance<br/> [changement de nom](/windows)<br/>

131

[Gestionnaire de licences des services Bureau à distance](/windows)<br/> [changement de nom](/windows)<br/>

132

Passerelle des services Bureau à distance<br/> [changement de nom](/windows)<br/>

133

Service Broker pour les connexions Bureau à distance<br/> [changement de nom](/windows)<br/>

134

Accès web au Bureau à distance<br/> [changement de nom](/windows)<br/>

322

Hôte de virtualisation des services Bureau à distance<br/>

Services de rôle serveur hôte de virtualisation des services Bureau à distance (322)

Valeur

Nom

325

[Services principaux](/windows)<br/>

327

[Graphiques virtuels Bureau à distance](/windows)<br/>

Services de rôle Services d’impression et de numérisation de document (7)

Valeur

Nom

135

Serveur d’impression

136

Impression Internet

137

Service d’impression LPD

328

[Serveur de numérisation distribuée](/windows)<br/>

Serveur Web (IIS)-services de rôle (2)

Valeur

Nom

140

Serveur web

141

Fonctionnalités HTTP communes

142

Contenu statique

143

Document par défaut

144

Parcourir le répertoire

145

Erreurs HTTP

146

Redirection HTTP

147

Développement d'applications

148

ASP.NET

149

Extensibilité .NET

150

ASP

151

CGI

152

Extensions ISAPI

153

Filtres ISAPI

154

Fichiers Include côté serveur

155

Intégrité et diagnostics

156

Journalisation HTTP

157

Outils de journalisation

158

Observateur de demandes

159

Traçage

160

Journalisation personnalisée

161

Journal ODBC

162

Sécurité

163

Authentification de base

164

Authentification Windows

165

Authentification Digest

166

Authentification par mappage de certificat client

167

Authentification par mappage de certificat client IIS

168

Autorisation URL

169

Filtrage des demandes

170

Restrictions IP et de domaine

171

Performances

172

Compression de contenu statique

173

compression du contenu dynamique

174

Outils des gestion

175

Console de gestion d’IIS

176

Scripts et outils de gestion IIS

177

Service d'administration

178

IIS 6 Management Compatibility

179

Compatibilité avec la métabase de données IIS 6

180

Compatibilité WMI d'IIS 6

181

Outils de script IIS 6

182

Console de gestion IIS 6

183

Service de publication FTP<br/>

184

Serveur FTP

185

Console de gestion FTP<br/>

314

Publication WebDAV

316

Service FTP<br/>

317

Extensibilité FTP<br/>

336

IIS Hostable Web Core<br/>

413

[ASP.NET 4.5](/windows)

414

[Extensibilité .NET 4.5](/windows)

445

[appialization](/windows)

446

[Prise en charge centralisée des certificats SSL](/windows)

447

[Protocole WebSocket](/windows)

Message Queuing-fonctionnalités (49)

Valeur

Nom

190

Services Message Queuing

191

Serveur Message Queuing

192

Intégration du service d’annuaire

193

Déclencheurs Message Queuing

194

Prise en charge HTTP

195

Service de routage

196

[prise en charge des clients Windows 2000](/windows)<br/>

197

Message Queuing DCOM Proxy

228

Prise en charge de la multidiffusion

Services de certificats Active Directory-Services de rôle (16)

Valeur

Nom

200

Autorité de certification

201

Inscription de l’autorité de certification via le Web

202

Répondeur en ligne

204

Service d’inscription de périphériques réseau

318

[Service Web Inscription de certificats](/windows)<br/>

319

[service Web Stratégie d'inscription de certificats](/windows)<br/>

stratégie réseau et Services de rôle Access Services (14)

Valeur

Nom

205

[Serveur de stratégie réseau](/windows)

206

[VPN](#vpn)

207

[Access Services à distance](/windows)

208

[Routage](#routing)

210

[Autorité HRA (Health Registration Authority)](/windows)

250

[Protocole d’autorisation des informations d’identification de l’hôte](/windows)

Services UDDI-services de rôle (11)

Valeur

Nom

215

[Application Web des services UDDI](/windows)<br/>

216

[Base de données des services UDDI](/windows)<br/>

Windows Service d’activation des processus-services de rôle (41)

Valeur

Nom

217

API de configuration

218

Environnement .NET

219

Modèle de processus

.NET Framework 3.5.1-fonctionnalités (36)

Valeur

Nom

220

.NET Framework 3.5.1<br/> [changement de nom](/windows)<br/>

221

Activation de Windows Communication Foundation

222

Activation HTTP

223

Activation non-HTTP

227

Visionneuse XPS<br/>

Services SNMP-fonctionnalités (59)

Valeur

Nom

224

[Service SNMP](/windows)

225

[Fournisseur WMI SNMP](/windows)

Services d’application-services de rôle

Valeur

Nom

230

[.NET Framework 3.5.1](/windows)<br/> [changement de nom](/windows)<br/>

231

[Prise en charge de Serveur Web (IIS)](/windows)

232

[Accès réseau COM+](/windows)

233

[Partage de port TCP](/windows)

234

[Windows Prise en charge du service d’activation des processus](/windows)

235

[Activation HTTP](/windows)

236

[Activation Message Queuing](/windows)

237

[Activation de TCP](/windows)

238

[Activation des canaux nommés](/windows)

239

[Transactions distribuées](/windows)

240

[Transactions distantes entrantes](/windows)

241

[Transactions distantes sortantes](/windows)

242

[Transactions WS-Automatic](/windows)

353

[Extensions du serveur d’applications pour .NET 4,0](/windows)<br/>

Windows Services de déploiement-rôle (19)

Valeur

Nom

251

Serveur de déploiement

252

Serveur de transport

services de rôle services AD RMS (Active Directory Rights Management Services) (17)

Valeur

Nom

253

Serveur AD RMS (Active Directory Rights Management Server)

254

Prise en charge de la fédération des identités

Outils d’administration de serveur distant (67)

Valeur

Nom

256

[Outils d’administration de rôles](/windows)

257

[Outils AD DS](/windows)<br/> [changement de nom](/windows)<br/>

258

[Outils de Snap-Ins et de Command-Line AD LDS](/windows)<br/> [changement de nom](/windows)<br/>

259

Outils de services de certificats Active Directory

260

[Network Policy and Access Services](/windows)

261

Outils de Services d’impression et de numérisation de document<br/> [changement de nom](/windows)<br/>

262

[Services AD RMS (Active Directory Rights Management Services)](/windows)

263

[Outils des services Bureau à distance](/windows)<br/> [changement de nom](/windows)<br/>

264

Windows Outils des services de déploiement

265

[Outils d’administration de fonctionnalités](/windows)

266

BitLocker Drive Encryption Tools

267

Outils d’extensions du serveur BITS

268

[Outils de clustering de basculement](/windows)

269

Outils d'équilibrage de la charge réseau

270

Outils du serveur SMTP

273

[Outils du serveur DNS](/windows)

277

Outils de services de fichiers

278

Outils de système de fichiers DFS

279

Outils de gestion des ressources pour serveur de fichiers

280

[Services pour les outils du système de fichiers réseau](/windows)

281

Outils de serveur Web (IIS)

284

[Outils de l’hôte de session Bureau à distance](/windows)<br/> [changement de nom](/windows)<br/>

285

Outils de passerelle Bureau à distance<br/> [changement de nom](/windows)<br/>

286

Outils de licence Bureau à distance<br/> [changement de nom](/windows)<br/>

288

Outils du serveur de télécopie

290

Outils du serveur WINS

291

[Outils des services UDDI](/windows)<br/>

292

Outils de l’autorité de certification

293

Outils de répondeur en ligne

297

[Outils de Serveur pour NIS](/windows)

299

[Composants logiciels enfichables et outils en ligne de commande AD DS](/windows)<br/> [changement de nom](/windows)<br/>

300

[Centre d’administration Active Directory](/windows)

301

Outils Hyper-V

323

[Visionneuse de mot de passe de récupération BitLocker](/windows)<br/>

326

[BitLocker Drive Encryption Administration Utilities](/windows)<br/>

329

[Outils AD DS et AD LDS](/windows)<br/>

330

Centre d'administration Active Directory<br/>

331

[Module Active Directory pour Windows PowerShell](/windows)<br/>

337

[Outils du Service Broker Connexion Bureau à distance](/windows)<br/>

410

[Client Gestion des adresses IP (IPAM)](/windows)

450

[Module Hyper-V pour Windows PowerShell](/windows)

462

[services AD RMS (Active Directory Rights Management Services) Tools](/windows)

465

[outil de gestion des partages et des Stockage](/windows)

471

[Outils de gestion de l’accès à distance](/windows)

472

[Module d’accès à distance pour Windows PowerShell](/windows)

473

[GUI d’accès à distance et outils de Command-Line](/windows)

474

[Outils Windows Server Update Services](/windows)

476

[Outils de diagnostic du gestionnaire de licences Bureau à distance](/windows)

479

[Outils SNMP](/windows)

480

[Outils d’activation en volume](/windows)

Windows Sauvegarde du serveur-fonctionnalités (39)

Valeur

Nom

296

[Sauvegarde Windows Server](/windows)

297

[Outils en ligne de commande](/windows)

Services de prise en charge de l’écriture manuscrite-fonctionnalités (310)

Valeur

Nom

311

[Prise en charge de l’encre](/windows)<br/>

312

[Reconnaissance de l’écriture manuscrite](/windows)<br/>

Service de transfert intelligent en arrière-plan (BITS)-fonctionnalités (335)

Valeur

Nom

54

Extension de serveur IIS

332

[Compact Server](/windows)<br/>

Prise en charge WOW64-fonctionnalités (340)

Valeur

Nom

341

[WoW64](#wow64)<br/>

342

[WoW64 pour .NET Framework 2,0 et Windows PowerShell](/windows)<br/>

343

[WoW64 pour .NET Framework 2,0](/windows)<br/>

344

[WoW64 pour PowerShell](/windows)<br/>

345

[WoW64 pour .NET Framework 3,0 et 3,5](/windows)<br/>

346

[WoW64 pour les services d’impression](/windows)<br/>

347

[WoW64 pour le clustering de basculement](/windows)<br/>

348

[WoW64 pour l’éditeur de méthode d’entrée](/windows)<br/>

349

[WoW64 pour le sous-système pour les Applications basées sur UNIX](/windows)<br/>

Interfaces utilisateur et services de rôle d’infrastructure (447)

Valeur

Nom

35

[Expérience utilisateur](/windows)

99

[Interpréteur de commandes graphique de serveur](/windows)

Windows Server Update Services-fonctionnalités (404)

Valeur

Nom

405

[API et applets de commande PowerShell](/windows)

406

[SQL Server Connectivité](/windows)

407

[Services WSUS](/windows)

408

[Console de gestion de l’interface utilisateur](/windows)

449

[Connectivité WID](/windows)

Windows PowerShell-fonctionnalités (417)

Valeur

Nom

411

[moteur Windows PowerShell 2,0](/windows)

412

[Windows PowerShell 3.0](/windows)

448

[Accès Web Windows PowerShell](/windows)

1 000

[Service de Desired State Configuration Windows PowerShell](/windows)

.NET Framework 4,5-fonctionnalités (418)

Valeur

Nom

419

[.NET Framework 4,5 étendu](/windows)

420

[Services WCF](/windows)

421

[Activation HTTP](/windows)

422

[Activation d’Message Queuing (MSMQ)](/windows)

423

[Activation de canaux nommés](/windows)

424

[Activation de TCP](/windows)

425

[Partage de port TCP](/windows)

429

[ASP.NET 4.5](/windows)

Accès à distance-rôle (468)

Valeur

Nom

469

[DirectAccess et VPN (RAS)](/windows)

470

[Routage](#routing)

Services de fichiers et de Stockage-rôle (481)

Valeur

Nom

482

[Services de stockage](/windows)

484

[Outils de gestion du cluster de basculement](/windows)



 

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Nom complet de la fonctionnalité serveur, par exemple « serveur de fichiers », « serveur d’impression » ou « expérience utilisateur ».

</dd> <dt>

**ID**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Numéro d’identification de la fonctionnalité de serveur parent. Cette propriété est 0 si la fonctionnalité représentée par l’instance actuelle de la classe n’a pas de fonctionnalité parente.

</dd> </dl>

## <a name="remarks"></a>Remarques

lisez le [Windows server 2008 Gestionnaire de serveur Technical Overview](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc753319(v=ws.10)) pour en savoir plus sur les fonctionnalités du serveur.

les entreprises qui n’utilisent pas de logiciel de gestion qui signale des fonctionnalités serveur, telles que System Center Operations Manager avec les packs d’administration installés, peuvent obtenir ces informations en interrogeant la classe **Win32 \_ ServerFeature** .

Vous pouvez utiliser les fonctionnalités de communication à distance de WMI ou WinRM pour récupérer les informations sur les fonctionnalités du serveur à partir des serveurs distants. Pour plus d’informations sur les connexions WMI DCOM à distance, consultez [connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md). Pour plus d’informations sur WinRM, consultez Gestion à distance de Windows.

Windows Server 2012 : **le \_ ServerFeature Win32** est déconseillé. Pour accéder aux informations sur les fonctionnalités de Windows Server par programme, vous pouvez utiliser les [applets](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/ee662311(v=technet.10))de commande gestionnaire de serveur.

### <a name="windows-server-2012-r2"></a>Windows Server 2012 R2

<dl> <dt>

<span id="Application_Server"></span><span id="application_server"></span><span id="APPLICATION_SERVER"></span>Serveur d’applications
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Streaming_Media_Services"></span><span id="streaming_media_services"></span><span id="STREAMING_MEDIA_SERVICES"></span>Media Services de diffusion en continu
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Active_Directory_Federation_Services"></span><span id="active_directory_federation_services"></span><span id="ACTIVE_DIRECTORY_FEDERATION_SERVICES"></span>services de fédération Active Directory (AD FS)
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="DHCP_Server"></span><span id="dhcp_server"></span><span id="DHCP_SERVER"></span>Serveur DHCP
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="DNS_Server"></span><span id="dns_server"></span><span id="DNS_SERVER"></span>Serveur DNS
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Remote_Desktop_Services"></span><span id="remote_desktop_services"></span><span id="REMOTE_DESKTOP_SERVICES"></span>Services Bureau à distance
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Windows_Server_Update_Services"></span><span id="windows_server_update_services"></span><span id="WINDOWS_SERVER_UPDATE_SERVICES"></span>Windows Server Update Services
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Failover_Clustering"></span><span id="failover_clustering"></span><span id="FAILOVER_CLUSTERING"></span>Clustering de basculement
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Network_Load_Balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>Équilibrage de la charge réseau
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id=".NET_Framework_3.5.1_Features"></span><span id=".net_framework_3.5.1_features"></span><span id=".NET_FRAMEWORK_3.5.1_FEATURES"></span>fonctionnalités de .NET Framework 3.5.1
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Windows_System_Resource_Manager"></span><span id="windows_system_resource_manager"></span><span id="WINDOWS_SYSTEM_RESOURCE_MANAGER"></span>Windows Gestionnaire des ressources système
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Windows_Server_Backup_Features"></span><span id="windows_server_backup_features"></span><span id="WINDOWS_SERVER_BACKUP_FEATURES"></span>Windows Fonctionnalités de sauvegarde du serveur
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Remote_Assistance"></span><span id="remote_assistance"></span><span id="REMOTE_ASSISTANCE"></span>Assistance à distance
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Telnet_Client"></span><span id="telnet_client"></span><span id="TELNET_CLIENT"></span>Client Telnet
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Telnet_Server"></span><span id="telnet_server"></span><span id="TELNET_SERVER"></span>Serveur Telnet
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Subsystem_For_Unix-based_Applications"></span><span id="subsystem_for_unix-based_applications"></span><span id="SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>Sous-système pour les applications UNIX
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Windows_Internal_Database"></span><span id="windows_internal_database"></span><span id="WINDOWS_INTERNAL_DATABASE"></span>Base de données interne Windows
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Storage_Manager_For_SANs"></span><span id="storage_manager_for_sans"></span><span id="STORAGE_MANAGER_FOR_SANS"></span>Stockage Gestionnaire pour réseau San
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Internet_Storage_Name_Server"></span><span id="internet_storage_name_server"></span><span id="INTERNET_STORAGE_NAME_SERVER"></span>serveur de noms Internet Stockage
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Multipath_I_O"></span><span id="multipath_i_o"></span><span id="MULTIPATH_I_O"></span>MPIO (Multipath I/O)
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="SNMP_Services"></span><span id="snmp_services"></span><span id="SNMP_SERVICES"></span>Services SNMP
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Services_For_Network_File_System"></span><span id="services_for_network_file_system"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM"></span>Services pour le système de fichiers réseau
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Peer_Name_Resolution_Protocol"></span><span id="peer_name_resolution_protocol"></span><span id="PEER_NAME_RESOLUTION_PROTOCOL"></span>Protocole PNRP (Peer Name Resolution Protocol)
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Remote_Server_Administration_Tools"></span><span id="remote_server_administration_tools"></span><span id="REMOTE_SERVER_ADMINISTRATION_TOOLS"></span>Outils d'administration de serveur distant
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Quality_Windows_Audio_Video_Experience"></span><span id="quality_windows_audio_video_experience"></span><span id="QUALITY_WINDOWS_AUDIO_VIDEO_EXPERIENCE"></span>expérience vidéo Audio Windows qualité
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Group_Policy_Management"></span><span id="group_policy_management"></span><span id="GROUP_POLICY_MANAGEMENT"></span>Gestion des stratégie de groupe
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Indexing_Service"></span><span id="indexing_service"></span><span id="INDEXING_SERVICE"></span>Service d’indexation
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="File_Server_Resource_Manager__FSRM_"></span><span id="file_server_resource_manager__fsrm_"></span><span id="FILE_SERVER_RESOURCE_MANAGER__FSRM_"></span>Gestionnaire des ressources de serveur de fichiers (FSRM)
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Windows_Server_Migration_Tools"></span><span id="windows_server_migration_tools"></span><span id="WINDOWS_SERVER_MIGRATION_TOOLS"></span>Windows Outils de migration de serveur
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="BranchCache"></span><span id="branchcache"></span><span id="BRANCHCACHE"></span>BranchCache
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="DirectAccess_Management_Console"></span><span id="directaccess_management_console"></span><span id="DIRECTACCESS_MANAGEMENT_CONSOLE"></span>Console de gestion DirectAccess
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Background_Intelligent_Transfer_Service__BITS_"></span><span id="background_intelligent_transfer_service__bits_"></span><span id="BACKGROUND_INTELLIGENT_TRANSFER_SERVICE__BITS_"></span>Service de transfert intelligent en arrière-plan (BITS)
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="WoW64_Support"></span><span id="wow64_support"></span><span id="WOW64_SUPPORT"></span>Prise en charge WoW64
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Window_Server_Update_Services"></span><span id="window_server_update_services"></span><span id="WINDOW_SERVER_UPDATE_SERVICES"></span>Services de mise à jour Windows Server
</dt> <dd>

Ajout

</dd> <dt>

<span id="IP_Address_Management__IPAM__Server"></span><span id="ip_address_management__ipam__server"></span><span id="IP_ADDRESS_MANAGEMENT__IPAM__SERVER"></span>serveur Gestion des adresses IP (IPAM)
</dt> <dd>

Ajout

</dd> <dt>

<span id="Windows_PowerShell"></span><span id="windows_powershell"></span><span id="WINDOWS_POWERSHELL"></span>Windows PowerShell
</dt> <dd>

Ajout

</dd> <dt>

<span id=".NET_Framework_4.5"></span><span id=".net_framework_4.5"></span><span id=".NET_FRAMEWORK_4.5"></span>.NET Framework 4,5
</dt> <dd>

Ajout

</dd> <dt>

<span id="Windows_Search_Service"></span><span id="windows_search_service"></span><span id="WINDOWS_SEARCH_SERVICE"></span>Windows Search Service
</dt> <dd>

Ajout

</dd> <dt>

<span id="Client_for_NFS"></span><span id="client_for_nfs"></span><span id="CLIENT_FOR_NFS"></span>Client pour NFS
</dt> <dd>

Ajout

</dd> <dt>

<span id="BitLocker_Network_Unlock"></span><span id="bitlocker_network_unlock"></span><span id="BITLOCKER_NETWORK_UNLOCK"></span>Déverrouillage réseau BitLocker
</dt> <dd>

Ajout

</dd> <dt>

<span id="Management_OData_IIS_Extension"></span><span id="management_odata_iis_extension"></span><span id="MANAGEMENT_ODATA_IIS_EXTENSION"></span>Extension IIS Management OData
</dt> <dd>

Ajout

</dd> <dt>

<span id=".NET_Framework_4.5_Advanced_Services"></span><span id=".net_framework_4.5_advanced_services"></span><span id=".NET_FRAMEWORK_4.5_ADVANCED_SERVICES"></span>Services avancés .NET Framework 4,5
</dt> <dd>

Ajout

</dd> <dt>

<span id=".NET_Framework_4.5_Features"></span><span id=".net_framework_4.5_features"></span><span id=".NET_FRAMEWORK_4.5_FEATURES"></span>fonctionnalités de .NET Framework 4,5
</dt> <dd>

Ajout

</dd> <dt>

<span id="User_Interfaces_and_Infrastructure"></span><span id="user_interfaces_and_infrastructure"></span><span id="USER_INTERFACES_AND_INFRASTRUCTURE"></span>Interfaces utilisateur et infrastructure
</dt> <dd>

Ajout

</dd> <dt>

<span id="Graphical_Management_Tools_and_Infrastructure"></span><span id="graphical_management_tools_and_infrastructure"></span><span id="GRAPHICAL_MANAGEMENT_TOOLS_AND_INFRASTRUCTURE"></span>Outils et infrastructure de gestion graphique
</dt> <dd>

Ajout

</dd> <dt>

<span id="File_and_Storage_Services"></span><span id="file_and_storage_services"></span><span id="FILE_AND_STORAGE_SERVICES"></span>Services de fichiers et de Stockage
</dt> <dd>

Ajout

</dd> <dt>

<span id="Windows_Server_Essentials_Experience"></span><span id="windows_server_essentials_experience"></span><span id="WINDOWS_SERVER_ESSENTIALS_EXPERIENCE"></span>Windows Expérience de Server Essentials
</dt> <dd>

Ajout

</dd> <dt>

<span id="Direct_Play"></span><span id="direct_play"></span><span id="DIRECT_PLAY"></span>Lecture directe
</dt> <dd>

Ajout

</dd> <dt>

<span id="Distributed_File_System"></span><span id="distributed_file_system"></span><span id="DISTRIBUTED_FILE_SYSTEM"></span>système de fichiers DFS
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="File_Server_Resource_Manager"></span><span id="file_server_resource_manager"></span><span id="FILE_SERVER_RESOURCE_MANAGER"></span>Gestionnaire des ressources du serveur de fichiers
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Services_For_Network_File_System"></span><span id="services_for_network_file_system"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM"></span>Services pour le système de fichiers réseau
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Single_Instance_Storage"></span><span id="single_instance_storage"></span><span id="SINGLE_INSTANCE_STORAGE"></span>Stockage d’Instance unique
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Windows_Search_Service"></span><span id="windows_search_service"></span><span id="WINDOWS_SEARCH_SERVICE"></span>Windows Search Service
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Indexing_Service"></span><span id="indexing_service"></span><span id="INDEXING_SERVICE"></span>Service d’indexation
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="iSCSI_Target_Storage_Provider__VDS_and_VSS_hardware_providers_"></span><span id="iscsi_target_storage_provider__vds_and_vss_hardware_providers_"></span><span id="ISCSI_TARGET_STORAGE_PROVIDER__VDS_AND_VSS_HARDWARE_PROVIDERS_"></span>fournisseur de Stockage de la cible iSCSI (fournisseurs de matériel VDS et VSS)
</dt> <dd>

Ajout

</dd> <dt>

<span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Dossiers de travail
</dt> <dd>

Ajout

</dd> <dt>

<span id="Active_Directory_Domain_Controller"></span><span id="active_directory_domain_controller"></span><span id="ACTIVE_DIRECTORY_DOMAIN_CONTROLLER"></span>Contrôleur de domaine Active Directory
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Identity_Management_For_Unix"></span><span id="identity_management_for_unix"></span><span id="IDENTITY_MANAGEMENT_FOR_UNIX"></span>Gestion des identités pour UNIX
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Server_For_Network_Information_Services"></span><span id="server_for_network_information_services"></span><span id="SERVER_FOR_NETWORK_INFORMATION_SERVICES"></span>Serveur pour Network Information Services
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Password_Synchronization"></span><span id="password_synchronization"></span><span id="PASSWORD_SYNCHRONIZATION"></span>Synchronisation de mot de passe
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Administration_Tools"></span><span id="administration_tools"></span><span id="ADMINISTRATION_TOOLS"></span>Outils d’administration
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Windows_Media_Server"></span><span id="windows_media_server"></span><span id="WINDOWS_MEDIA_SERVER"></span>Windows Serveur multimédia
</dt> <dd>

N'est plus pris en charge.

</dd> <dt>

<span id="Web-based_Administration"></span><span id="web-based_administration"></span><span id="WEB-BASED_ADMINISTRATION"></span>Administration basée sur le Web
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Logging_Agent"></span><span id="logging_agent"></span><span id="LOGGING_AGENT"></span>Agent de journalisation
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Federation_Service"></span><span id="federation_service"></span><span id="FEDERATION_SERVICE"></span>service FS (Federation Service)
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Federation_Service_Policy"></span><span id="federation_service_policy"></span><span id="FEDERATION_SERVICE_POLICY"></span>Stratégie de service FS (Federation Service)
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="AD_FS_Web_Agents"></span><span id="ad_fs_web_agents"></span><span id="AD_FS_WEB_AGENTS"></span>Agents Web AD FS
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Windows_Token-based_Agent"></span><span id="windows_token-based_agent"></span><span id="WINDOWS_TOKEN-BASED_AGENT"></span>Windows Agent basé sur les jetons
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Remote_Desktop_Licensing"></span><span id="remote_desktop_licensing"></span><span id="REMOTE_DESKTOP_LICENSING"></span>Licences Bureau à distance
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Network_Policy_Server"></span><span id="network_policy_server"></span><span id="NETWORK_POLICY_SERVER"></span>NPS (Network Policy Server)
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="VPN"></span><span id="vpn"></span>VPN
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Remote_Access_Services"></span><span id="remote_access_services"></span><span id="REMOTE_ACCESS_SERVICES"></span>Access Services à distance
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Routing"></span><span id="routing"></span><span id="ROUTING"></span>Achemine
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Health_Registration_Authority"></span><span id="health_registration_authority"></span><span id="HEALTH_REGISTRATION_AUTHORITY"></span>Autorité d’inscription d’intégrité
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Host_Credential_Authorization_Protocol"></span><span id="host_credential_authorization_protocol"></span><span id="HOST_CREDENTIAL_AUTHORIZATION_PROTOCOL"></span>Protocole d’autorisation des informations d’identification de l’hôte
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id=".NET_Framework_3.5.1"></span><span id=".net_framework_3.5.1"></span><span id=".NET_FRAMEWORK_3.5.1"></span>.NET Framework 3.5.1
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="XPS_Viewer"></span><span id="xps_viewer"></span><span id="XPS_VIEWER"></span>Visionneuse XPS
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="SNMP_Service"></span><span id="snmp_service"></span><span id="SNMP_SERVICE"></span>Service SNMP
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="SNMP_WMI_Provider"></span><span id="snmp_wmi_provider"></span><span id="SNMP_WMI_PROVIDER"></span>Fournisseur WMI SNMP
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id=".NET_Framework_3.5.1"></span><span id=".net_framework_3.5.1"></span><span id=".NET_FRAMEWORK_3.5.1"></span>.NET Framework 3.5.1
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Web_Server__IIS__Support"></span><span id="web_server__iis__support"></span><span id="WEB_SERVER__IIS__SUPPORT"></span>Prise en charge du serveur Web (IIS)
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="COM__Network_Access"></span><span id="com__network_access"></span><span id="COM__NETWORK_ACCESS"></span>Accès réseau COM+
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="TCP_Port_Sharing"></span><span id="tcp_port_sharing"></span><span id="TCP_PORT_SHARING"></span>Partage de port TCP
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Windows_Process_Activation_Service_Support"></span><span id="windows_process_activation_service_support"></span><span id="WINDOWS_PROCESS_ACTIVATION_SERVICE_SUPPORT"></span>Windows Prise en charge du service d’activation des processus
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="HTTP_Activation"></span><span id="http_activation"></span><span id="HTTP_ACTIVATION"></span>Activation HTTP
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Message_Queuing_Activation"></span><span id="message_queuing_activation"></span><span id="MESSAGE_QUEUING_ACTIVATION"></span>Activation Message Queuing
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="TCP_Activation"></span><span id="tcp_activation"></span><span id="TCP_ACTIVATION"></span>Activation TCP
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Named_Pipes_Activation"></span><span id="named_pipes_activation"></span><span id="NAMED_PIPES_ACTIVATION"></span>Activation des canaux nommés
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Distributed_Transactions"></span><span id="distributed_transactions"></span><span id="DISTRIBUTED_TRANSACTIONS"></span>Transactions distribuées
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Incoming_Remote_Transactions"></span><span id="incoming_remote_transactions"></span><span id="INCOMING_REMOTE_TRANSACTIONS"></span>Transactions distantes entrantes
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Outgoing_Remote_Transactions"></span><span id="outgoing_remote_transactions"></span><span id="OUTGOING_REMOTE_TRANSACTIONS"></span>Transactions distantes sortantes
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="WS-Automatic_Transactions"></span><span id="ws-automatic_transactions"></span><span id="WS-AUTOMATIC_TRANSACTIONS"></span>Transactions WS-Automatic
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Application_Server_Extensions_for_.NET_4.0"></span><span id="application_server_extensions_for_.net_4.0"></span><span id="APPLICATION_SERVER_EXTENSIONS_FOR_.NET_4.0"></span>Extensions du serveur d’applications pour .NET 4,0
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Role_Administration_Tools"></span><span id="role_administration_tools"></span><span id="ROLE_ADMINISTRATION_TOOLS"></span>Outils d’administration de rôles
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="AD_DS_Tools"></span><span id="ad_ds_tools"></span><span id="AD_DS_TOOLS"></span>Outils de AD DS
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="AD_LDS_Snap-Ins_and_Command-Line_Tools"></span><span id="ad_lds_snap-ins_and_command-line_tools"></span><span id="AD_LDS_SNAP-INS_AND_COMMAND-LINE_TOOLS"></span>Outils de Snap-Ins et de Command-Line AD LDS
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Network_Policy_and_Access_Services"></span><span id="network_policy_and_access_services"></span><span id="NETWORK_POLICY_AND_ACCESS_SERVICES"></span>Stratégie réseau et Access Services
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Active_Directory_Rights_Management_Services"></span><span id="active_directory_rights_management_services"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES"></span>services AD RMS (Active Directory Rights Management Services)
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Remote_Desktop_Services_Tools"></span><span id="remote_desktop_services_tools"></span><span id="REMOTE_DESKTOP_SERVICES_TOOLS"></span>Outils de Services Bureau à distance
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Feature_Administration_Tools"></span><span id="feature_administration_tools"></span><span id="FEATURE_ADMINISTRATION_TOOLS"></span>Outils d’administration de fonctionnalités
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Failover_Clustering_Tools"></span><span id="failover_clustering_tools"></span><span id="FAILOVER_CLUSTERING_TOOLS"></span>Outils de clustering de basculement
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="DNS_Server_Tools"></span><span id="dns_server_tools"></span><span id="DNS_SERVER_TOOLS"></span>Outils du serveur DNS
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Services_For_Network_File_System_Tools"></span><span id="services_for_network_file_system_tools"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM_TOOLS"></span>Services pour les outils du système de fichiers réseau
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Web_Server__IIS__Tools"></span><span id="web_server__iis__tools"></span><span id="WEB_SERVER__IIS__TOOLS"></span>Outils de serveur Web (IIS)
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Server_for_NIS_Tools"></span><span id="server_for_nis_tools"></span><span id="SERVER_FOR_NIS_TOOLS"></span>Outils de Serveur pour NIS
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="AD_DS_Snap-Ins_and_Command-Line_Tools"></span><span id="ad_ds_snap-ins_and_command-line_tools"></span><span id="AD_DS_SNAP-INS_AND_COMMAND-LINE_TOOLS"></span>Outils de Snap-Ins et de Command-Line AD DS
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>Outils de AD DS et de AD LDS
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Remote_Desktop_Connection_Broker_Tools"></span><span id="remote_desktop_connection_broker_tools"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_TOOLS"></span>Outils du Service Broker Connexion Bureau à distance
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="IP_Address_Management__IPAM__Client"></span><span id="ip_address_management__ipam__client"></span><span id="IP_ADDRESS_MANAGEMENT__IPAM__CLIENT"></span>Client Gestion des adresses IP (IPAM)
</dt> <dd>

Ajout

</dd> <dt>

<span id="Hyper-V_Module_for_Windows_PowerShell"></span><span id="hyper-v_module_for_windows_powershell"></span><span id="HYPER-V_MODULE_FOR_WINDOWS_POWERSHELL"></span>Module Hyper-V pour Windows PowerShell
</dt> <dd></dd> <dt>

<span id="Active_Directory_Rights_Management_Services_Tool"></span><span id="active_directory_rights_management_services_tool"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES_TOOL"></span>services AD RMS (Active Directory Rights Management Services) Outil
</dt> <dd>

Ajout

</dd> <dt>

<span id="Share_and_Storage_Management_Tool"></span><span id="share_and_storage_management_tool"></span><span id="SHARE_AND_STORAGE_MANAGEMENT_TOOL"></span>outil de gestion des partages et des Stockage
</dt> <dd>

Ajout

</dd> <dt>

<span id="Remote_Access_Management_Tools"></span><span id="remote_access_management_tools"></span><span id="REMOTE_ACCESS_MANAGEMENT_TOOLS"></span>Outils de gestion de l’accès à distance
</dt> <dd>

Ajout

</dd> <dt>

<span id="Remote_Access_module_for_Windows_PowerShell"></span><span id="remote_access_module_for_windows_powershell"></span><span id="REMOTE_ACCESS_MODULE_FOR_WINDOWS_POWERSHELL"></span>Module d’accès à distance pour Windows PowerShell
</dt> <dd>

Ajout

</dd> <dt>

<span id="Remote_Access_GUI_and_Command-Line_Tools"></span><span id="remote_access_gui_and_command-line_tools"></span><span id="REMOTE_ACCESS_GUI_AND_COMMAND-LINE_TOOLS"></span>GUI d’accès à distance et outils de Command-Line
</dt> <dd>

Ajout

</dd> <dt>

<span id="Windows_Server_Update_Services_Tools"></span><span id="windows_server_update_services_tools"></span><span id="WINDOWS_SERVER_UPDATE_SERVICES_TOOLS"></span>Windows Server Update Services Tools
</dt> <dd>

Ajout

</dd> <dt>

<span id="Remote_Desktop_Licensing_Diagnoser_Tools"></span><span id="remote_desktop_licensing_diagnoser_tools"></span><span id="REMOTE_DESKTOP_LICENSING_DIAGNOSER_TOOLS"></span>Outils de diagnostic du gestionnaire de licences Bureau à distance
</dt> <dd>

Ajout

</dd> <dt>

<span id="SNMP_Tools"></span><span id="snmp_tools"></span><span id="SNMP_TOOLS"></span>Outils SNMP
</dt> <dd>

Ajout

</dd> <dt>

<span id="Volume_Activation_Tools"></span><span id="volume_activation_tools"></span><span id="VOLUME_ACTIVATION_TOOLS"></span>Outils d’activation en volume
</dt> <dd>

Ajout

</dd> <dt>

<span id="Windows_Server_Backup"></span><span id="windows_server_backup"></span><span id="WINDOWS_SERVER_BACKUP"></span>Windows Sauvegarde du serveur
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Command_Line_Tools"></span><span id="command_line_tools"></span><span id="COMMAND_LINE_TOOLS"></span>Outils en ligne de commande
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Ink_Support"></span><span id="ink_support"></span><span id="INK_SUPPORT"></span>Prise en charge de l’encre
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Handwriting_Recognition"></span><span id="handwriting_recognition"></span><span id="HANDWRITING_RECOGNITION"></span>Reconnaissance de l’écriture manuscrite
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Compact_Server"></span><span id="compact_server"></span><span id="COMPACT_SERVER"></span>Serveur compact
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="WoW64"></span><span id="wow64"></span><span id="WOW64"></span>WoW64
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="WoW64_for_.NET_Framework_2.0_and___________"></span><span id="wow64_for_.net_framework_2.0_and___________"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0_AND___________"></span>WoW64 pour .NET Framework 2,0 et PowerShell
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="WoW64_for_.NET_Framework_2.0"></span><span id="wow64_for_.net_framework_2.0"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0"></span>WoW64 pour .NET Framework 2,0
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="WoW64_for___________"></span><span id="wow64_for___________"></span><span id="WOW64_FOR___________"></span>WoW64 pour PowerShell
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="WoW64_for_.NET_Framework_3.0_and_3.5"></span><span id="wow64_for_.net_framework_3.0_and_3.5"></span><span id="WOW64_FOR_.NET_FRAMEWORK_3.0_AND_3.5"></span>WoW64 pour .NET Framework 3,0 et 3,5
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="WoW64_for_Print_Services"></span><span id="wow64_for_print_services"></span><span id="WOW64_FOR_PRINT_SERVICES"></span>WoW64 pour les services d’impression
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="WoW64_for_Failover_Clustering"></span><span id="wow64_for_failover_clustering"></span><span id="WOW64_FOR_FAILOVER_CLUSTERING"></span>WoW64 pour le clustering de basculement
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="WoW64_for_Input_Method_Editor"></span><span id="wow64_for_input_method_editor"></span><span id="WOW64_FOR_INPUT_METHOD_EDITOR"></span>WoW64 pour l’éditeur de méthode d’entrée
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="WoW64_for_Subsystem_for_UNIX-based_Applications"></span><span id="wow64_for_subsystem_for_unix-based_applications"></span><span id="WOW64_FOR_SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>WoW64 pour le sous-système pour les Applications basées sur UNIX
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Desktop_Experience"></span><span id="desktop_experience"></span><span id="DESKTOP_EXPERIENCE"></span>Expérience utilisateur
</dt> <dd>

Ajout

</dd> <dt>

<span id="Server_Graphical_Shell"></span><span id="server_graphical_shell"></span><span id="SERVER_GRAPHICAL_SHELL"></span>Interpréteur de commandes graphique de serveur
</dt> <dd>

Ajout

</dd> <dt>

<span id="API_and_PowerShell_cmdlets"></span><span id="api_and_powershell_cmdlets"></span><span id="API_AND_POWERSHELL_CMDLETS"></span>API et applets de commande PowerShell
</dt> <dd>

Ajout

</dd> <dt>

<span id="SQL_Server_Connectivity"></span><span id="sql_server_connectivity"></span><span id="SQL_SERVER_CONNECTIVITY"></span>SQL Server Connectivité
</dt> <dd>

Ajout

</dd> <dt>

<span id="WSUS_Services"></span><span id="wsus_services"></span><span id="WSUS_SERVICES"></span>Services WSUS
</dt> <dd>

Ajout

</dd> <dt>

<span id="User_Interface_Management_Console"></span><span id="user_interface_management_console"></span><span id="USER_INTERFACE_MANAGEMENT_CONSOLE"></span>Console de gestion de l’interface utilisateur
</dt> <dd>

Ajout

</dd> <dt>

<span id="WID_Connectivity"></span><span id="wid_connectivity"></span><span id="WID_CONNECTIVITY"></span>Connectivité WID
</dt> <dd>

Ajout

</dd> <dt>

<span id="Windows_PowerShell_2.0_Engine"></span><span id="windows_powershell_2.0_engine"></span><span id="WINDOWS_POWERSHELL_2.0_ENGINE"></span>moteur Windows PowerShell 2,0
</dt> <dd>

Ajout

</dd> <dt>

<span id="Windows_PowerShell_3.0"></span><span id="windows_powershell_3.0"></span><span id="WINDOWS_POWERSHELL_3.0"></span>Windows PowerShell 3,0
</dt> <dd>

Ajout

</dd> <dt>

<span id="Windows_PowerShell_Web_Access"></span><span id="windows_powershell_web_access"></span><span id="WINDOWS_POWERSHELL_WEB_ACCESS"></span>Windows PowerShell Accès web
</dt> <dd>

Ajout

</dd> <dt>

<span id="Windows_PowerShell_Desired_State_Configuration_Service"></span><span id="windows_powershell_desired_state_configuration_service"></span><span id="WINDOWS_POWERSHELL_DESIRED_STATE_CONFIGURATION_SERVICE"></span>Service de Desired State Configuration Windows PowerShell
</dt> <dd>

Ajout

</dd> <dt>

<span id=".NET_Framework_4.5_Extended"></span><span id=".net_framework_4.5_extended"></span><span id=".NET_FRAMEWORK_4.5_EXTENDED"></span>.NET Framework 4,5 étendu
</dt> <dd>

Ajout

</dd> <dt>

<span id="WCF_Services"></span><span id="wcf_services"></span><span id="WCF_SERVICES"></span>Services WCF
</dt> <dd>

Ajout

</dd> <dt>

<span id="HTTP_Activation"></span><span id="http_activation"></span><span id="HTTP_ACTIVATION"></span>Activation HTTP
</dt> <dd>

Ajout

</dd> <dt>

<span id="Message_Queuing__MSMQ__Activation"></span><span id="message_queuing__msmq__activation"></span><span id="MESSAGE_QUEUING__MSMQ__ACTIVATION"></span>Activation d’Message Queuing (MSMQ)
</dt> <dd></dd> <dt>

<span id="Named_Pipe_Activation"></span><span id="named_pipe_activation"></span><span id="NAMED_PIPE_ACTIVATION"></span>Activation du canal nommé
</dt> <dd>

Ajout

</dd> <dt>

<span id="TCP_Activation"></span><span id="tcp_activation"></span><span id="TCP_ACTIVATION"></span>Activation TCP
</dt> <dd>

Ajout

</dd> <dt>

<span id="TCP_Port_Sharing"></span><span id="tcp_port_sharing"></span><span id="TCP_PORT_SHARING"></span>Partage de port TCP
</dt> <dd>

Ajout

</dd> <dt>

<span id="ASP.NET_4.5"></span><span id="asp.net_4.5"></span>ASP.NET 4,5
</dt> <dd>

Ajout

</dd> <dt>

<span id=".NET_Extensibility_4.5"></span><span id=".net_extensibility_4.5"></span><span id=".NET_EXTENSIBILITY_4.5"></span>Extensibilité .NET 4,5
</dt> <dd>

Ajout

</dd> <dt>

<span id="DirectAccess_and_VPN__RAS_"></span><span id="directaccess_and_vpn__ras_"></span><span id="DIRECTACCESS_AND_VPN__RAS_"></span>DirectAccess et VPN (RAS)
</dt> <dd>

Ajout

</dd> <dt>

<span id="Routing"></span><span id="routing"></span><span id="ROUTING"></span>Achemine
</dt> <dd>

Ajout

</dd> <dt>

<span id="Storage_Services"></span><span id="storage_services"></span><span id="STORAGE_SERVICES"></span>Stockage Services
</dt> <dd>

Ajout

</dd> <dt>

<span id="Failover_Cluster_Management_Tools"></span><span id="failover_cluster_management_tools"></span><span id="FAILOVER_CLUSTER_MANAGEMENT_TOOLS"></span>Outils de gestion du cluster de basculement
</dt> <dd>

Ajout

</dd> <dt>

<span id="Active_Directory_Rights_Management_Services_Tools"></span><span id="active_directory_rights_management_services_tools"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES_TOOLS"></span>services AD RMS (Active Directory Rights Management Services) Tools
</dt> <dd>

Ajout

</dd> <dt>

<span id="Application_Initialization"></span><span id="application_initialization"></span><span id="APPLICATION_INITIALIZATION"></span>Initialisation d’application
</dt> <dd>

Ajout

</dd> <dt>

<span id="Centralized_SSL_Certificate_Support"></span><span id="centralized_ssl_certificate_support"></span><span id="CENTRALIZED_SSL_CERTIFICATE_SUPPORT"></span>Prise en charge centralisée des certificats SSL
</dt> <dd>

Ajout

</dd> <dt>

<span id="Claims-aware_Agent"></span><span id="claims-aware_agent"></span><span id="CLAIMS-AWARE_AGENT"></span>Agent prenant en charge les revendications
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Remote_Desktop_Session_Host_Tools"></span><span id="remote_desktop_session_host_tools"></span><span id="REMOTE_DESKTOP_SESSION_HOST_TOOLS"></span>Outils de l’hôte de session Bureau à distance
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="WebSocket_Protocol"></span><span id="websocket_protocol"></span><span id="WEBSOCKET_PROTOCOL"></span>Protocole WebSocket
</dt> <dd>

n’est plus pris en charge

</dd> <dt>

<span id="COM__Network_Access"></span><span id="com__network_access"></span><span id="COM__NETWORK_ACCESS"></span>Accès réseau COM+
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="File_and_iSCSI_Services_name_change"></span><span id="file_and_iscsi_services_name_change"></span><span id="FILE_AND_ISCSI_SERVICES_NAME_CHANGE"></span>Modification du nom des services de fichiers et iSCSI
</dt> <dd>

Modification des services de fichiers

</dd> </dl>

### <a name="windows-server-2012"></a>Windows Server 2012

<dl> <dt>

<span id="User_Interfaces_and_Infrastructure"></span><span id="user_interfaces_and_infrastructure"></span><span id="USER_INTERFACES_AND_INFRASTRUCTURE"></span>Interfaces utilisateur et infrastructure
</dt> <dd>

Ajout

</dd> <dt>

<span id="Server_for_NFS"></span><span id="server_for_nfs"></span><span id="SERVER_FOR_NFS"></span>Serveur pour NFS
</dt> <dd>

Ajout

</dd> <dt>

<span id="File_Server_VSS_Agent_Service"></span><span id="file_server_vss_agent_service"></span><span id="FILE_SERVER_VSS_AGENT_SERVICE"></span>Service agent VSS du serveur de fichiers
</dt> <dd>

Ajout

</dd> <dt>

<span id="iSCSI_Target_Server"></span><span id="iscsi_target_server"></span><span id="ISCSI_TARGET_SERVER"></span>Serveur cible iSCSI
</dt> <dd>

Ajout

</dd> <dt>

<span id="Data_Deduplication"></span><span id="data_deduplication"></span><span id="DATA_DEDUPLICATION"></span>Déduplication des données
</dt> <dd>

Ajout

</dd> <dt>

<span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Dossiers de travail
</dt> <dd>

Supprimé

</dd> <dt>

<span id="Core_Services"></span><span id="core_services"></span><span id="CORE_SERVICES"></span>Services principaux
</dt> <dd>

Ajouté pour cette version uniquement.

</dd> <dt>

<span id="Remote_Desktop_Virtual_Graphics"></span><span id="remote_desktop_virtual_graphics"></span><span id="REMOTE_DESKTOP_VIRTUAL_GRAPHICS"></span>Graphiques virtuels Bureau à distance
</dt> <dd>

Ajouté pour cette version uniquement

</dd> <dt>

<span id="Remote_Access"></span><span id="remote_access"></span><span id="REMOTE_ACCESS"></span>Accès à distance
</dt> <dd>

Ajout

</dd> </dl>

### <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

<dl> <dt>

<span id="UDDI_Services"></span><span id="uddi_services"></span><span id="UDDI_SERVICES"></span>Services UDDI
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Windows_System_Resource_Manager"></span><span id="windows_system_resource_manager"></span><span id="WINDOWS_SYSTEM_RESOURCE_MANAGER"></span>Windows Gestionnaire des ressources système
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Removable_Storage_Manager"></span><span id="removable_storage_manager"></span><span id="REMOVABLE_STORAGE_MANAGER"></span>gestionnaire de Stockage amovible
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Windows_PowerShell"></span><span id="windows_powershell"></span><span id="WINDOWS_POWERSHELL"></span>Windows PowerShell
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Ink_and_Handwriting_Services"></span><span id="ink_and_handwriting_services"></span><span id="INK_AND_HANDWRITING_SERVICES"></span>Services de prise en charge de l'écriture manuscrite
</dt> <dd>

Ajout

</dd> <dt>

<span id="WinRM_IIS_Extension"></span><span id="winrm_iis_extension"></span><span id="WINRM_IIS_EXTENSION"></span>Extension WinRM IIS
</dt> <dd>

Ajout

</dd> <dt>

<span id="DirectAccess_Management_Console"></span><span id="directaccess_management_console"></span><span id="DIRECTACCESS_MANAGEMENT_CONSOLE"></span>Console de gestion DirectAccess
</dt> <dd>

Ajout

</dd> <dt>

<span id="Background_Intelligent_Transfer_Service__BITS_"></span><span id="background_intelligent_transfer_service__bits_"></span><span id="BACKGROUND_INTELLIGENT_TRANSFER_SERVICE__BITS_"></span>Service de transfert intelligent en arrière-plan (BITS)
</dt> <dd>

Ajout

</dd> <dt>

<span id="XPS_Viewer"></span><span id="xps_viewer"></span><span id="XPS_VIEWER"></span>Visionneuse XPS
</dt> <dd>

Ajout

</dd> <dt>

<span id="Windows_Biometric_Framework"></span><span id="windows_biometric_framework"></span><span id="WINDOWS_BIOMETRIC_FRAMEWORK"></span>Windows Infrastructure biométrique
</dt> <dd>

Ajout

</dd> <dt>

<span id="WoW64_Support"></span><span id="wow64_support"></span><span id="WOW64_SUPPORT"></span>Prise en charge WoW64
</dt> <dd>

Ajout

</dd> <dt>

<span id="Windows_PowerShell_Integrated_Scripting_Environment__ISE_"></span><span id="windows_powershell_integrated_scripting_environment__ise_"></span><span id="WINDOWS_POWERSHELL_INTEGRATED_SCRIPTING_ENVIRONMENT__ISE_"></span>Windows PowerShell Environnement d’écriture de scripts intégré (ISE)
</dt> <dd>

Ajout

</dd> <dt>

<span id="File_Replication_Service"></span><span id="file_replication_service"></span><span id="FILE_REPLICATION_SERVICE"></span>Service de réplication de fichiers
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="BranchCache_for_Network_Files"></span><span id="branchcache_for_network_files"></span><span id="BRANCHCACHE_FOR_NETWORK_FILES"></span>BranchCache pour fichiers réseau
</dt> <dd>

Ajout

</dd> <dt>

<span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Dossiers de travail
</dt> <dd>

Ajout

</dd> <dt>

<span id="Distributed_Scan_Server"></span><span id="distributed_scan_server"></span><span id="DISTRIBUTED_SCAN_SERVER"></span>Serveur de numérisation distribuée
</dt> <dd>

Ajout

</dd> <dt>

<span id="FTP_Publishing_Service"></span><span id="ftp_publishing_service"></span><span id="FTP_PUBLISHING_SERVICE"></span>Service de publication FTP
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="FTP_Management_Console"></span><span id="ftp_management_console"></span><span id="FTP_MANAGEMENT_CONSOLE"></span>Console de gestion FTP
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="FTP_Service"></span><span id="ftp_service"></span><span id="FTP_SERVICE"></span>Service FTP
</dt> <dd>

Ajout

</dd> <dt>

<span id="FTP_Extensibility"></span><span id="ftp_extensibility"></span><span id="FTP_EXTENSIBILITY"></span>Extensibilité FTP
</dt> <dd>

Ajout

</dd> <dt>

<span id="IIS_Hostable_Web_Core"></span><span id="iis_hostable_web_core"></span><span id="IIS_HOSTABLE_WEB_CORE"></span>Noyau Web hébergé par IIS
</dt> <dd></dd> <dt>

<span id="Windows_2000_Client_Support"></span><span id="windows_2000_client_support"></span><span id="WINDOWS_2000_CLIENT_SUPPORT"></span>prise en charge des clients Windows 2000
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Certificate_Enrollment_Web_Service"></span><span id="certificate_enrollment_web_service"></span><span id="CERTIFICATE_ENROLLMENT_WEB_SERVICE"></span>service Web Inscription de certificats
</dt> <dd>

Ajout

</dd> <dt>

<span id="Certificate_Enrollment_Policy_Web_Service"></span><span id="certificate_enrollment_policy_web_service"></span><span id="CERTIFICATE_ENROLLMENT_POLICY_WEB_SERVICE"></span>service Web Stratégie d'inscription de certificats
</dt> <dd>

Ajout

</dd> <dt>

<span id="UDDI_Services_Web_Application"></span><span id="uddi_services_web_application"></span><span id="UDDI_SERVICES_WEB_APPLICATION"></span>Application Web des services UDDI
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="UDDI_Services_Database"></span><span id="uddi_services_database"></span><span id="UDDI_SERVICES_DATABASE"></span>Base de données des services UDDI
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="Application_Server_Extensions_for_.NET_4.0"></span><span id="application_server_extensions_for_.net_4.0"></span><span id="APPLICATION_SERVER_EXTENSIONS_FOR_.NET_4.0"></span>Extensions du serveur d’applications pour .NET 4,0
</dt> <dd>

Ajout

</dd> <dt>

<span id="UDDI_Services_Tools"></span><span id="uddi_services_tools"></span><span id="UDDI_SERVICES_TOOLS"></span>Outils des services UDDI
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="BitLocker_Drive_Encryption_Administration_Utilities"></span><span id="bitlocker_drive_encryption_administration_utilities"></span><span id="BITLOCKER_DRIVE_ENCRYPTION_ADMINISTRATION_UTILITIES"></span>Utilitaires d’administration de Chiffrement de lecteur BitLocker
</dt> <dd>

Ajout

</dd> <dt>

<span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>Outils de AD DS et de AD LDS
</dt> <dd>

Plus pris en charge

</dd> <dt>

<span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>Outils de AD DS et de AD LDS
</dt> <dd>

Ajout

</dd> <dt>

<span id="Active_Directory_Administrative_Center"></span><span id="active_directory_administrative_center"></span><span id="ACTIVE_DIRECTORY_ADMINISTRATIVE_CENTER"></span>Centre d'administration Active Directory
</dt> <dd>

Ajout

</dd> <dt>

<span id="Active_Directory_module_for___________Windows_PowerShell"></span><span id="active_directory_module_for___________windows_powershell"></span><span id="ACTIVE_DIRECTORY_MODULE_FOR___________WINDOWS_POWERSHELL"></span>Module Active Directory pour Windows PowerShell
</dt> <dd>

Ajout

</dd> <dt>

<span id="Remote_Desktop_Connection_Broker_Tools"></span><span id="remote_desktop_connection_broker_tools"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_TOOLS"></span>Outils du Service Broker Connexion Bureau à distance
</dt> <dd>

Ajout

</dd> <dt>

<span id="WoW64"></span><span id="wow64"></span><span id="WOW64"></span>WoW64
</dt> <dd>

Ajout

</dd> <dt>

<span id="WoW64_for_.NET_Framework_2.0_and_Windows_PowerShell"></span><span id="wow64_for_.net_framework_2.0_and_windows_powershell"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0_AND_WINDOWS_POWERSHELL"></span>WoW64 pour .NET Framework 2,0 et Windows PowerShell
</dt> <dd>

Ajout

</dd> <dt>

<span id="WoW64_for_.NET_Framework_2.0"></span><span id="wow64_for_.net_framework_2.0"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0"></span>WoW64 pour .NET Framework 2,0
</dt> <dd>

Ajout

</dd> <dt>

<span id="WoW64_for___________"></span><span id="wow64_for___________"></span><span id="WOW64_FOR___________"></span>WoW64 pour PowerShell
</dt> <dd>

Ajout

</dd> <dt>

<span id="WoW64_for_.NET_Framework_3.0_and_3.5"></span><span id="wow64_for_.net_framework_3.0_and_3.5"></span><span id="WOW64_FOR_.NET_FRAMEWORK_3.0_AND_3.5"></span>WoW64 pour .NET Framework 3,0 et 3,5
</dt> <dd>

Ajout

</dd> <dt>

<span id="WoW64_for_Print_Services"></span><span id="wow64_for_print_services"></span><span id="WOW64_FOR_PRINT_SERVICES"></span>WoW64 pour les services d’impression
</dt> <dd>

Ajout

</dd> <dt>

<span id="WoW64_for_Failover_Clustering"></span><span id="wow64_for_failover_clustering"></span><span id="WOW64_FOR_FAILOVER_CLUSTERING"></span>WoW64 pour le clustering de basculement
</dt> <dd>

Ajout

</dd> <dt>

<span id="WoW64_for_Input_Method_Editor"></span><span id="wow64_for_input_method_editor"></span><span id="WOW64_FOR_INPUT_METHOD_EDITOR"></span>WoW64 pour l’éditeur de méthode d’entrée
</dt> <dd>

Ajout

</dd> <dt>

<span id="WoW64_for_Subsystem_for_UNIX-based_Applications"></span><span id="wow64_for_subsystem_for_unix-based_applications"></span><span id="WOW64_FOR_SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>WoW64 pour le sous-système pour les Applications basées sur UNIX
</dt> <dd>

Ajout

</dd> <dt>

<span id="BitLocker_Recovery_Password_Viewer"></span><span id="bitlocker_recovery_password_viewer"></span><span id="BITLOCKER_RECOVERY_PASSWORD_VIEWER"></span>Visionneuse de mot de passe de récupération BitLocker
</dt> <dd>

Ajout

</dd> <dt>

<span id="Print_and_Document_Services_name_change"></span><span id="print_and_document_services_name_change"></span><span id="PRINT_AND_DOCUMENT_SERVICES_NAME_CHANGE"></span>Modification du nom de Services d’impression et de numérisation de document
</dt> <dd>

Services d’impression nommés pour cette version

</dd> <dt>

<span id="Remote_Desktop_Services_name_change"></span><span id="remote_desktop_services_name_change"></span><span id="REMOTE_DESKTOP_SERVICES_NAME_CHANGE"></span>Modification du nom de Services Bureau à distance
</dt> <dd>

Services Terminal Server nommés dans cette version

</dd> <dt>

<span id=".NET_Framework_3.5.1_Features_name_change"></span><span id=".net_framework_3.5.1_features_name_change"></span><span id=".NET_FRAMEWORK_3.5.1_FEATURES_NAME_CHANGE"></span>modification du nom des fonctionnalités .NET Framework 3.5.1
</dt> <dd>

fonctionnalités nommées .NET Framework 3,0 dans cette version

</dd> <dt>

<span id="Remote_Desktop_Session_Host_name_change"></span><span id="remote_desktop_session_host_name_change"></span><span id="REMOTE_DESKTOP_SESSION_HOST_NAME_CHANGE"></span>Modification du nom d’hôte de session Bureau à distance
</dt> <dd>

Terminal Server nommé dans cette version

</dd> <dt>

<span id="Remote_Desktop_Licensing_name_change"></span><span id="remote_desktop_licensing_name_change"></span><span id="REMOTE_DESKTOP_LICENSING_NAME_CHANGE"></span>Modification du nom du gestionnaire de Bureau à distance
</dt> <dd>

Licences TS nommées dans cette version

</dd> <dt>

<span id="Remote_Desktop_Gateway_name_change"></span><span id="remote_desktop_gateway_name_change"></span><span id="REMOTE_DESKTOP_GATEWAY_NAME_CHANGE"></span>Modification du nom de la passerelle Bureau à distance
</dt> <dd>

Passerelle TS nommée dans cette version

</dd> <dt>

<span id="Remote_Desktop_Connection_Broker_name_change"></span><span id="remote_desktop_connection_broker_name_change"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_NAME_CHANGE"></span>Modification du nom de l’Connexion Bureau à distance Broker
</dt> <dd>

Session Broker TS nommée dans cette version

</dd> <dt>

<span id="Remote_Desktop_Web_Access_name_change"></span><span id="remote_desktop_web_access_name_change"></span><span id="REMOTE_DESKTOP_WEB_ACCESS_NAME_CHANGE"></span>Modification du nom de la Bureau à distance Accès web
</dt> <dd>

Accès web TS nommé dans cette version

</dd> <dt>

<span id=".NET_Framework_3.5.1_name_change"></span><span id=".net_framework_3.5.1_name_change"></span><span id=".NET_FRAMEWORK_3.5.1_NAME_CHANGE"></span>modification du nom de .NET Framework 3.5.1
</dt> <dd>

(220) fonctionnalités .net FX 3,0 nommées dans cette version

(230) nommé Core de serveur d’applications dans cette version

</dd> <dt>

<span id="AD_DS_Tools_name_change"></span><span id="ad_ds_tools_name_change"></span><span id="AD_DS_TOOLS_NAME_CHANGE"></span>Modification du nom des outils de AD DS
</dt> <dd>

Outils nommés Active Directory Domain Services dans cette version

</dd> <dt>

<span id="AD_LDS_Snap-Ins_and_Command-Line_Tools_name_change"></span><span id="ad_lds_snap-ins_and_command-line_tools_name_change"></span><span id="AD_LDS_SNAP-INS_AND_COMMAND-LINE_TOOLS_NAME_CHANGE"></span>Modification du nom des outils de AD LDS Snap-Ins et Command-Line
</dt> <dd>

Outils nommés services AD LDS (Active Directory Lightweight Directory Services) dans cette version

</dd> <dt>

<span id="Print_and_Document_Services_Tools_name_change"></span><span id="print_and_document_services_tools_name_change"></span><span id="PRINT_AND_DOCUMENT_SERVICES_TOOLS_NAME_CHANGE"></span>Modification du nom des outils de Services d’impression et de numérisation de document
</dt> <dd>

Outils des services d’impression nommés dans cette version

</dd> <dt>

<span id="Remote_Desktop_Services_Tools_name_change"></span><span id="remote_desktop_services_tools_name_change"></span><span id="REMOTE_DESKTOP_SERVICES_TOOLS_NAME_CHANGE"></span>Modification du nom des outils de Services Bureau à distance
</dt> <dd>

Outils des services Terminal Server dans cette version

</dd> <dt>

<span id="Remote_Desktop_Session_Host_Tools_name_change"></span><span id="remote_desktop_session_host_tools_name_change"></span><span id="REMOTE_DESKTOP_SESSION_HOST_TOOLS_NAME_CHANGE"></span>Modification du nom des outils de l’hôte de session Bureau à distance
</dt> <dd>

Outils nommés Terminal Server dans cette version

</dd> <dt>

<span id="Remote_Desktop_Gateway_Tools_name_change"></span><span id="remote_desktop_gateway_tools_name_change"></span><span id="REMOTE_DESKTOP_GATEWAY_TOOLS_NAME_CHANGE"></span>Modification du nom des outils de passerelle Bureau à distance
</dt> <dd>

Outils de passerelle TS nommés dans cette version

</dd> <dt>

<span id="Remote_Desktop_Licensing_Tools_name_change"></span><span id="remote_desktop_licensing_tools_name_change"></span><span id="REMOTE_DESKTOP_LICENSING_TOOLS_NAME_CHANGE"></span>Modification du nom des outils de licence Bureau à distance
</dt> <dd>

Outils de gestion de licences TS nommés dans cette version

</dd> <dt>

<span id="AD_DS_Snap-Ins_and_Command-Line_Tools_name_change"></span><span id="ad_ds_snap-ins_and_command-line_tools_name_change"></span><span id="AD_DS_SNAP-INS_AND_COMMAND-LINE_TOOLS_NAME_CHANGE"></span>Modification du nom des outils de AD DS Snap-Ins et Command-Line
</dt> <dd>

Outils du contrôleur de domaine Active Directory

</dd> </dl>

## <a name="examples"></a>Exemples

Le script suivant affiche les noms de toutes les fonctionnalités du serveur sur l’ordinateur nommé « FABRIKAM ». notez que l’ordinateur cible doit exécuter Windows server 2008 ou un système d’exploitation serveur ultérieur.


```VB
strComputer = "FABRIKAM"

Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")

Set colFeatureList = objWMIService.ExecQuery("SELECT Name FROM Win32_ServerFeature")

For Each objFeature In colFeatureList
   WScript.Echo objFeature.Name

Next
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>ServerCompProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>ServerCompProv.dll</dt> </dl> |



 

